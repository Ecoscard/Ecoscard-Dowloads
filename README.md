# Downloads oficiais Ecoscard

Pacotes compilados das aplicações Ecoscard para clientes e ambientes autorizados. Cada aplicação é publicada em [Releases](../../releases); este README mostra a versão atual de cada uma.

## Aplicações disponíveis

<!-- BEGIN ecoscard-dataprep-multos-privatesmart-config -->
### Ecoscard DataPrep MULTOS PrivateSmart Config

Aplicação web para gerar as configurações DataPrep MULTOS PrivateSmart (RegistryDetail, Template Private, PaymentKeys, ALT/ALR/DAT), os componentes de chaves TDES e os PDFs da cerimônia de chaves.

| Item | Valor |
| --- | --- |
| Nome técnico | `ecoscard-dataprep-multos-privatesmart-config` (antes `EcosDataPrepConfigMultosPrivateSmart`) |
| Versão atual | [2.8.0](../../releases/tag/ecosdataprep-v2.8.0) — 06/11/2026 |
| Download | [`EcosDataPrepconfigMultosPrivateSmart.zip`](../../releases/download/ecosdataprep-v2.8.0/EcosDataPrepconfigMultosPrivateSmart.zip) |
| SHA-256 | `7cf92b13ee40a69f671c32ae0d683a199d5d4777e7c47a94c1643d4af2922b3f` |
| Plataforma | Windows x64 |
| Execução | `start.ps1`, abre em `http://127.0.0.1:5080` |
<!-- END ecoscard-dataprep-multos-privatesmart-config -->

### EcosWorkerHSMGateway

Serviço TCP que valida criptogramas EMV (comando A1: ARQC e ARPC com Tag 91) direto no HSM via PKCS#11.

| Item | Valor |
| --- | --- |
| Nome técnico | `ecoscard-hsmgateway-worker` (antes `EcosWorkerHSMGateway`) |
| Versão atual | [20.26.11.10](../../releases/tag/EcosWorkerHSMGateway-v20.26.11.10) — 10/11/2026 |
| Download | [`EcosWorkerHSMGateway.zip`](../../releases/download/EcosWorkerHSMGateway-v20.26.11.10/EcosWorkerHSMGateway.zip) |
| SHA-256 | `f450b8355ecf152b5f82c70f8334d87aa1798fa6f161e6449e93b92ea92d0d58` |
| Plataforma | Windows e Linux (.NET 8) |

### EcosDataPrepNetCore

Serviço de processamento DataPrep (Worker Service com RabbitMQ e Serilog).

| Item | Valor |
| --- | --- |
| Nome técnico | `ecoscard-dataprep-api` (antes `EcosDataPrepNetCore`) |
| Versão atual | [20.26.11.9](../../releases/tag/ecosdataprepnetcore-v20.26.11.9) — 09/11/2026 |
| Download | [`EcosDataPrepNetCore8.zip`](../../releases/download/ecosdataprepnetcore-v20.26.11.9/EcosDataPrepNetCore8.zip) |
| SHA-256 | `aa30b3997cb15ded2c819f83cc495c411feef1daeb1ae4ef226918205b092e35` |
| Plataforma | Windows (serviço) e Linux (.NET 8) |

<!-- BEGIN ecoscard-dataprep-client-worker -->
### Ecoscard DataPrep Client

Cliente DataPrep que envia arquivos de embossing à API DataPrep e grava os arquivos de personalização. Roda em modo console (um arquivo) ou worker (monitora uma pasta, também como serviço Windows).

| Item | Valor |
| --- | --- |
| Nome técnico | `ecoscard-dataprep-client-worker` (antes `EcosDataPrep.Client`) |
| Versão atual | [20.26.11.19-r5](../../releases/tag/ecoscard-dataprep-client-worker-20.26.11.19-r5) — 19/11/2026 |
| Download | [`ecoscard-dataprep-client-worker-20.26.11.19-r5-win-x64.zip`](../../releases/download/ecoscard-dataprep-client-worker-20.26.11.19-r5/ecoscard-dataprep-client-worker-20.26.11.19-r5-win-x64.zip) |
| SHA-256 | `90bf691c33819da233c3484c44b5c92b19e583683b094f1ca2519363d01a3d39` |
| Plataforma | Windows x64 (self-contained, não exige .NET instalado) |
| Execução | `start-worker.bat` (monitora pasta) ou `start-console.bat` (um arquivo); serviço com `install-windows-service.ps1` |
<!-- END ecoscard-dataprep-client-worker -->

<!-- BEGIN ecoscard-dataprep-configeditor-web -->
### Ecoscard DataPrep ConfigEditor

Editor web das configurações do DataPrep (Bootstrap, ProjectProcessing e projetos da API), com validação, diagrama 3D, prévia de payloads e extração de ALU MULTOS.

| Item | Valor |
| --- | --- |
| Nome técnico | `ecoscard-dataprep-configeditor-web` (antes `EcosDataPrepConfigEditorGitRepo`) |
| Versão atual | [20.26.11.19-r5](../../releases/tag/ecoscard-dataprep-configeditor-web-20.26.11.19-r5) — 19/11/2026 |
| Download | [`ecoscard-dataprep-configeditor-web-20.26.11.19-r5-win-x64.zip`](../../releases/download/ecoscard-dataprep-configeditor-web-20.26.11.19-r5/ecoscard-dataprep-configeditor-web-20.26.11.19-r5-win-x64.zip) |
| SHA-256 | `902cdcd204d80833c4c316b9d749b7d4fc43a6a781c02c3effd3edd1dcb51d55` |
| Plataforma | Windows x64 (self-contained, não exige .NET instalado); Docker `suporte472/ecoscard-dataprep-configeditor-web` |
| Execução | `start.bat`, abre em `http://127.0.0.1:5098` |
<!-- END ecoscard-dataprep-configeditor-web -->

## Como instalar

1. Abra a versão atual da aplicação na tabela acima ou em [Releases](../../releases).
2. Baixe o arquivo ZIP e confira o SHA-256:
   - Windows (PowerShell): `Get-FileHash .\arquivo.zip -Algorithm SHA256`
   - Linux: `sha256sum arquivo.zip`
3. Extraia o conteúdo em uma pasta local.
4. Siga as notas da release para configurar e executar a aplicação.

## Versões

As versões seguem a data do build no formato `YY.YY.M.D`: `20.26.11.19` corresponde a 19/11/2026. Uma segunda publicação no mesmo dia recebe o sufixo `-r2`. Releases a partir de 19/11/2026 usam a tag `<nome-técnico>-<versão>`, por exemplo `ecoscard-dataprep-multos-privatesmart-config-20.26.11.19`. Versões publicadas não são substituídas.

## Suporte

Fale com o suporte Ecoscard informando a aplicação, a versão e o SHA-256 do pacote utilizado.
