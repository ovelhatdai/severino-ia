# Severino.ia 0.4.0 — instalar e trabalhar

Para Diulia e Guilherme, no DES Advocacia. Aplicativo para Mac Apple Silicon e Intel, com macOS 13 ou superior.

## Instalar ou atualizar

1. Baixe o DMG protegido na página de versões do GitHub indicada pelo Vinicius. Abra o arquivo e informe a senha do instalador recebida separadamente.
2. Arraste Severino.ia.app para Aplicativos. Em uma atualização, feche a versão anterior antes de substituir o aplicativo.
3. Abra o Severino. Se o macOS impedir a abertura por desenvolvedor não verificado, confira a origem com Vinicius e siga o fluxo que o próprio macOS apresentar em Privacidade e Segurança. O aplicativo ainda não tem notarização Apple.

Os dados ficam em `~/Library/Application Support/SeverinoIA`. A senha do DMG protege a abertura do instalador; cada pessoa usa seu próprio acesso ao AdvOS e ao tribunal.

## Conectar o AdvOS

1. Clique em **Conectar ao AdvOS** e **Entrar pelo navegador**.
2. Entre com seu próprio usuário do AdvOS. Confira a solicitação antes de autorizá-la. Esta versão usa o fluxo oficial compatível `advos-cli`, que aparece como CLI na página do AdvOS. A solicitação foi iniciada pelo Severino.ia. **Approve** significa **Aprovar acesso**.
3. Aguarde **AdvOS conectado**, com seu nome e o escritório DES. Se a sessão estiver em outro escritório, o aplicativo pede a seleção da DES antes de continuar.

A sessão fica no Keychain, o cofre de senhas do macOS. Não cole tokens, senhas ou códigos no chat. Se o Mac pedir acesso ao cofre, confira o aplicativo e a informação solicitada. **Sair do AdvOS** esquece a sessão neste Mac.

## Receber os processos

Clique em **Sincronizar AdvOS** e escolha uma fonte:

- **Minha fila de petições:** itens atribuídos ao seu usuário na fila de petições do AdvOS.
- **Processos sob minha responsabilidade:** processos judiciais ativos atribuídos ao seu usuário.
- **Carteira TRF4 ativa do escritório:** processos disponíveis ao seu usuário, para revisão. Essa opção não atribui responsável nem aprova os processos.
- **Consultar um processo pelo número:** busca exata do CNJ.

Esta versão recebe processos de primeiro grau do TRF4 em PR, RS e SC. Uma fonte vazia não significa ausência de trabalho no Kanban, nas checklists ou no Drive. A sincronização preserva observações e documentos locais; vínculo divergente é marcado como conflito. Ela não inicia protocolo automaticamente.

## Montar a petição

1. Selecione o processo na fila e use **Criar trabalho com documentos do AdvOS**. Em **Peticionar**, clique em **Puxar documentos do AdvOS**.
2. Confira cliente e processo. Marque apenas a peça final revisada e os anexos necessários. Documentos de outro processo do cliente aparecem identificados para sua conferência.
3. Use **Baixar selecionados para o pacote**. PDFs preservam os bytes originais. Imagens são convertidas em PDF e exigem conferência de legibilidade; outros formatos precisam de conversão antes de anexar. Mudança nos documentos invalida a aprovação anterior.
4. Confira a ordem, o evento, o tipo e o sigilo de cada arquivo. Salve a classificação e registre a referência da aprovação específica. O Guilherme valida e opera; as peças e o certificado continuam em nome da Daiane.
5. Abra o portal, faça login diretamente no tribunal, leia os eventos e confira o prazo e eventual resposta já existente. A preparação e o protocolo exigem confirmação do pacote específico. Certificado, PIN, captcha e autenticação adicional são operados pela pessoa autorizada.

O adaptador JFPR permanece em piloto acompanhado. PR, RS e SC precisam de prova operacional do envio em sua própria unidade. Petições iniciais, correção jurídica automática e protocolo em lote não fazem parte desta versão. Não dê ciência em intimações ao baixar documentos.

## Devolver o comprovante ao AdvOS

Depois do protocolo, importe o **comprovante oficial**, confira processo, evento, data e resultado e use **Devolver comprovante ao AdvOS**. Confira o destino e o tipo do documento antes de confirmar.

O PDF é anexado com visibilidade restrita ao cliente e ao processo conferidos. O Severino consulta o registro e baixa o arquivo recebido novamente para comparar seu SHA-256, a identificação dos bytes. Só então mostra **Comprovante confirmado no AdvOS**. O retorno não muda automaticamente o estado do processo nem encerra prazos.

Se a resposta se perder ou houver divergência, confira o AdvOS antes de repetir. O controle local permite reconciliar uma tentativa recebida pelo servidor. Não execute o mesmo retorno simultaneamente em dois Macs: a API atual não oferece reserva central deste trabalho.

## O que já foi verificado e o que falta

Login, sincronização de um processo e download de PDF foram conferidos na interface do aplicativo com o AdvOS publicado. O retorno de comprovante foi validado com servidor simulado, inclusive perda da resposta após cadastro. O primeiro retorno com comprovante real ainda precisa ser acompanhado. Instalação em cada Mac e protocolo real no tribunal exigem conferência própria.

Suporte: Vinicius. Não inclua dados de clientes em issues públicas do GitHub.
