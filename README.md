# Severino.ia

Aplicativo Mac para fila de processos, conferência de arquivos e preparação acompanhada de petições intermediárias no eproc.

**Versão 0.4.0 — piloto acompanhado.** O instalador está protegido por senha. Este repositório publica apenas documentação e o pacote criptografado; o código-fonte do aplicativo não está publicado.

## Baixar e instalar

[**Baixar instalador protegido para Mac**](https://github.com/ovelhatdai/severino-ia/releases/download/v0.4.0/Severino.ia-0.4.0-Mac-protegido.dmg)

[Ver a versão e os arquivos disponíveis](https://github.com/ovelhatdai/severino-ia/releases/tag/v0.4.0) · [Instruções de instalação](INSTALACAO.md)

1. Baixe o arquivo `.dmg` pelo link acima.
2. Abra o arquivo e informe a senha recebida do responsável pela distribuição. Não marque a opção de salvar a senha em computador compartilhado.
3. Arraste **Severino.ia.app** para **Aplicativos**.
4. Ejete a imagem e abra **Severino.ia** em Aplicativos.
5. A instalação começa com a fila vazia. Conecte seu próprio usuário ao AdvOS, confira o escritório DES e escolha a fonte em **Sincronizar AdvOS**, ou importe o CSV autorizado. Selecione apenas a peça final revisada e os anexos necessários.

**Compatibilidade:** macOS 13 ou superior; Mac com Apple Silicon ou Intel. Não precisa instalar Python, Node.js ou Xcode. Esta versão não é para Windows.

## Primeira abertura no macOS

Este piloto tem assinatura local ad-hoc e ainda não foi autenticado pela Apple (notarização). O Mac pode exibir um aviso na primeira abertura. Confira que o download veio deste repositório e consulte o [procedimento oficial da Apple](https://support.apple.com/pt-br/102445). A aprovação da abertura é uma ação da pessoa que usa o Mac. O pacote não desativa proteções de segurança.

## O que está disponível

- Login individual no AdvOS com sessão guardada no Keychain do Mac, usando o fluxo oficial compatível identificado como CLI.
- Sincronização de fila de petições, processos atribuídos, carteira TRF4 ativa ou consulta por CNJ, para revisão.
- Recebimento dos PDFs escolhidos no AdvOS, com conferência de cliente/processo e invalidação da aprovação quando o pacote muda.
- Retorno explícito de comprovante restrito ao cadastro conferido, com releitura e confronto de SHA-256; primeiro retorno real ainda precisa ser acompanhado.
- Importação de fila em CSV de processos do TRF4 de primeiro grau, PR/RS/SC.
- Conferência de PDFs e ZIPs por abertura, número do processo, páginas, partes e SHA-256.
- Organização de peça e anexos em um pacote com ordem, tipo e sigilo por PDF.
- Registro da aprovação específica informada pelo operador e conferência dos eventos recentes.
- Adaptador acompanhado de preparação da movimentação e solicitação de protocolo após confirmação do pacote exato.
- Histórico, comprovante oficial associado e exportação de handoff.

Login, sincronização de processo e download de PDF foram conferidos na interface com o AdvOS publicado. O retorno do comprovante foi testado com transporte simulado, inclusive perda de resposta após cadastro; a primeira operação real ainda está pendente.

## Limites do piloto

A automação de peticionamento foi calibrada no formulário da **JFPR**. Ainda falta validar um fluxo completo de upload, retorno do protocolo e comprovante no tribunal. **JFRS e JFSC precisam de validação própria.** TRF2, TRF6, TJs e PJe estão fora do suporte desta versão. A pessoa escolhe os documentos do AdvOS que entram no pacote. A versão não gera ou corrige minutas por IA e não ativa integração direta com ChatGPT ou Claude Code.

Login, senha, PIN, OTP, CAPTCHA, certificado e revisão jurídica permanecem com a pessoa autorizada. O aplicativo não considera um clique, upload ou preparação como prova de protocolo: é preciso conferir o retorno e o comprovante oficial. Opções/prazos marcados para encerramento interrompem a automação para conclusão humana.

O perfil de aprovação desta distribuição é Guilherme Barbosa. O registro é uma declaração do operador, vinculada ao pacote exato; não autentica a decisão jurídica nem substitui representação no processo. Cada pessoa faz login com a credencial autorizada para o caso.

## Dados e senha

O instalador não inclui clientes, processos, autos, minutas, cookies ou credenciais do escritório. Os dados importados ficam no perfil local de quem instalou, em `~/Library/Application Support/SeverinoIA`.

A senha protege a abertura do instalador com criptografia AES-256. Ela não é uma licença individual: quem tiver o arquivo e a senha poderá abri-lo. O aplicativo não bloqueia cópias após a instalação nem possui revogação por usuário. A senha não está neste repositório; solicite-a ao responsável.

O arquivo `SHA256SUMS.txt` da versão permite conferir a integridade do download. Os arquivos “Source code” gerados automaticamente pelo GitHub contêm somente a documentação deste repositório, não o aplicativo: use o instalador `.dmg`.
