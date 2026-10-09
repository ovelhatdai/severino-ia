# Severino.ia

Aplicativo Mac para fila de processos, conferência de arquivos e preparação acompanhada de petições intermediárias no eproc.

**Versão 0.2.2 — piloto acompanhado.** O instalador está protegido por senha. Este repositório publica apenas documentação e o pacote criptografado; o código-fonte do aplicativo não está publicado.

## Baixar e instalar

[**Baixar instalador protegido para Mac**](https://github.com/ovelhatdai/severino-ia/releases/download/v0.2.2/Severino.ia-0.2.2-Mac-protegido.dmg)

[Ver a versão e os arquivos disponíveis](https://github.com/ovelhatdai/severino-ia/releases/tag/v0.2.2) · [Instruções de instalação](INSTALACAO.md)

1. Baixe o arquivo `.dmg` pelo link acima.
2. Abra o arquivo e informe a senha recebida do responsável pela distribuição. Não marque a opção de salvar a senha em computador compartilhado.
3. Arraste **Severino.ia.app** para **Aplicativos**.
4. Ejete a imagem e abra **Severino.ia** em Aplicativos.
5. A instalação começa com a fila vazia. Importe o CSV autorizado da sua fila e selecione as peças e os anexos aprovados para cada processo.

**Compatibilidade:** macOS 13 ou superior; Mac com Apple Silicon ou Intel. Não precisa instalar Python, Node.js ou Xcode. Esta versão não é para Windows.

## Primeira abertura no macOS

Este piloto tem assinatura local ad-hoc e ainda não foi autenticado pela Apple (notarização). O Mac pode exibir um aviso na primeira abertura. Confira que o download veio deste repositório e consulte o [procedimento oficial da Apple](https://support.apple.com/pt-br/102445). A aprovação da abertura é uma ação da pessoa que usa o Mac. O pacote não desativa proteções de segurança.

## O que está disponível

- Importação de fila em CSV de processos do TRF4 de primeiro grau, PR/RS/SC.
- Conferência de PDFs e ZIPs por abertura, número do processo, páginas, partes e SHA-256.
- Organização de peça e anexos em um pacote com ordem, tipo e sigilo por PDF.
- Registro da aprovação específica informada pelo operador e conferência dos eventos recentes.
- Adaptador acompanhado de preparação da movimentação e solicitação de protocolo após confirmação do pacote exato.
- Histórico, comprovante oficial associado e exportação de handoff.

## Limites do piloto

A automação de peticionamento foi calibrada no formulário da **JFPR**. Ainda falta validar um fluxo completo de upload, retorno do protocolo e comprovante no tribunal. **JFRS e JFSC precisam de validação própria.** TRF2, TRF6, TJs e PJe estão fora do suporte desta versão. A versão não importa automaticamente minutas do painel ou do AdvOS.

Login, senha, PIN, OTP, CAPTCHA, certificado e revisão jurídica permanecem com a pessoa autorizada. O aplicativo não considera um clique, upload ou preparação como prova de protocolo: é preciso conferir o retorno e o comprovante oficial. Opções/prazos marcados para encerramento interrompem a automação para conclusão humana.

O perfil de aprovação desta distribuição é Guilherme Barbosa. O registro é uma declaração do operador, vinculada ao pacote exato; não autentica a decisão jurídica nem substitui representação no processo. Cada pessoa faz login com a credencial autorizada para o caso.

## Dados e senha

O instalador não inclui clientes, processos, autos, minutas, cookies ou credenciais do escritório. Os dados importados ficam no perfil local de quem instalou, em `~/Library/Application Support/SeverinoIA`.

A senha protege a abertura do instalador com criptografia AES-256. Ela não é uma licença individual: quem tiver o arquivo e a senha poderá abri-lo. O aplicativo não bloqueia cópias após a instalação nem possui revogação por usuário. A senha não está neste repositório; solicite-a ao responsável.

O arquivo `SHA256SUMS.txt` da versão permite conferir a integridade do download. Os arquivos “Source code” gerados automaticamente pelo GitHub contêm somente a documentação deste repositório, não o aplicativo: use o instalador `.dmg`.
