# Instalação do Severino.ia 0.2.2 no Mac

## Requisitos

- macOS 13 ou superior.
- Mac Intel ou Apple Silicon.
- Senha do instalador recebida do responsável pela distribuição.

## Instalar

1. Baixe `Severino.ia-0.2.2-Mac-protegido.dmg` em https://github.com/ovelhatdai/severino-ia/releases/tag/v0.2.2.
2. Abra o arquivo. O macOS pedirá a senha para abrir a imagem criptografada.
3. Digite a senha exatamente como foi recebida, respeitando maiúsculas, minúsculas e pontuação. Não publique a senha nem a salve em um computador compartilhado.
4. Dentro da janela, arraste **Severino.ia.app** para o atalho **Aplicativos**. Se o Mac pedir autorização de administrador para copiar, essa é a senha do usuário do Mac, diferente da senha do instalador.
5. Ejete a imagem. Abra o aplicativo em **Aplicativos**.

## Aviso da Apple na primeira abertura

O piloto ainda não tem autenticação da Apple/notarização. Se houver aviso, a pessoa responsável pelo Mac deve conferir a origem e seguir a [orientação oficial da Apple](https://support.apple.com/pt-br/102445). Não use comandos para desativar proteções nem remover quarentena. Um alerta de arquivo danificado ou conteúdo mal-intencionado exige parar e comunicar o responsável, em vez de forçar a abertura.

## Primeiro uso

A fila começa vazia. Na tela principal, use **Importar CSV** e escolha o controle autorizado do TRF4 de primeiro grau. Para cada processo, escolha **Criar trabalho de peticionamento**, selecione apenas a peça final revisada e os anexos corretos, confira ordem/tipos/sigilos e registre a referência da liberação jurídica específica.

O PDF dos autos completos é material de consulta e auditoria; não substitui a peça e seus anexos. O aplicativo não converte automaticamente Word/Markdown em PDF. A integração com minutas do painel/AdvOS ainda não está disponível.

A sessão do eproc dentro do aplicativo é própria: faça o login diretamente nela. Certificado, PIN, OTP, CAPTCHA e revisão jurídica são humanos. O primeiro piloto precisa conferir uploads, pendência preparada, retorno do protocolo e comprovante no tribunal. Consulte os limites no README antes de usar outra unidade.

## Verificar o arquivo

Baixe também `SHA256SUMS.txt`. Se desejar verificar a integridade no Terminal, execute na pasta de downloads:

```
shasum -a 256 -c SHA256SUMS.txt
```

## Atualizar

Feche o Severino antes de substituir o aplicativo. Preserve `~/Library/Application Support/SeverinoIA`: é onde ficam a fila, as observações e os pacotes locais. O instalador não inclui nem modifica esses dados. Não substitua a pasta de dados por uma cópia de outro cliente ou operador.
