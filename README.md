# Como configurar/instalar o `Microsoft Office 2016` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para instalar/configurar o `Microsoft Office 2016` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings to install/configure the `Microsoft Office 2016` on `Linux Ubuntu`._


## Descrição [2]

### `Microsoft Office 2016`

O `Microsoft Office 2016` é uma suíte de aplicativos de produtividade lançada pela `Microsoft`, que oferece ferramentas essenciais tanto para usuários domésticos quanto para empresas. Inclui programas populares como `Word`, `Excel`, `PowerPoint`, `Outlook`, `Access` e `Publisher`, cada um com funções específicas que vão desde a criação de documentos de texto e gerenciamento de _e-mails_, até análise de dados e apresentações dinâmicas. O `Office 2016` trouxe melhorias significativas em colaboração e segurança, integrando-se com o `OneDrive` e outros serviços em nuvem, e apresentando recursos como a coautoria em tempo real e a proteção de dados avançada, refletindo as necessidades de um ambiente de trabalho mais conectado e seguro.


## 1. Como baixar o arquivo `.iso` do `Microsoft Office 2016`

1. Acessar o _website_ <https://massgrave.dev/>

<div align="center">
    <img src="docs/figures/massgrave_homepage.png" alt="Minha Imagem" />
    <p>Fig. 1. https://massgrave.dev. </p>
</div>

2. Clicar em `Download Windows/Office`

<div align="center">
    <img src="docs/figures/massgrave_download_windows_office.png" alt="Minha Imagem" />
    <p>Fig. 2. https://massgrave.dev/#Download__How_to_use_it.</p>
</div>


3. Clicar em `Office MSI VL (Old versions)`

<div align="center">
    <img src="docs/figures/massgrave_genuine_installation_media.png" alt="Minha Imagem" />
    <p>Fig. 3. https://massgrave.dev/genuine-installation-media.html#Verify_Authenticity_Of_Files.</p>
</div>


4. Clicar em `Office MSI VL Download`

<div align="center">
    <img src="docs/figures/massgrave_office_msi_vl_download.png" alt="Minha Imagem" />
    <p>Fig. 4. `Office MSI VL Download`.</p>
</div>


5. Clicar me `Office 2016 Pro Plus`

<div align="center">
    <img src="docs/figures/massgrave_office_2016_pro_plus_downloads.png" alt="Minha Imagem" />
    <p>Fig. 5. `Office 2016 Pro Plus`.</p>
</div>


6. Clicar me `SW_DVD5_Office_Professional_Plus_2016_W32_English_MLF_X20-41353.ISO`

<div align="center">
    <img src="docs/figures/massgrave_office_2016_english_x86_iso_download.png" alt="Minha Imagem" />
    <p>Fig. 6. `SW_DVD5_Office_Professional_Plus_2016_W32_English_MLF_X20-41353.ISO`.</p>
</div>

7. Salvar a imagem `.ISO` em `~/Downloads`, mantendo o nome do arquivo indicado na etapa anterior.

## 2. Configurar/Instalar/Usar o `wine` para a versão mais atualizada e estável

Para configurar/instalar/usar o `Wine` no `Linux Ubuntu`, você pode seguir os passos abaixo:

1. **Aqui está um guia passo a passo**: `https://github.com/edftechnology/wine`


## 3. Configurar/Instalar/Usar o `playonlinux` para a versão mais atualizada e estável

Para configurar/instalar/usar o `PlayOnLinux (POL)` no `Linux Ubuntu`, consulte também o guia do repositório: <https://github.com/edftechnology/playonlinux>.

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. O instalador deste documento requer o _runner_ `Wine x86` na versão `5.8`. Na raiz deste
repositório, copie-os da pasta `docs/PlayOnLinux wine` para o diretório do `PlayOnLinux`:

    ```bash
    mkdir -pv "$HOME/.PlayOnLinux/wine/linux-x86"
    cp -a "docs/PlayOnLinux wine/linux-x86/5.8" \
          "$HOME/.PlayOnLinux/wine/linux-x86/"
    ```

3. Conferir se os quatro diretórios aparecem em `~/.PlayOnLinux/wine/linux-x86/`:

    ```bash
    ls -lah "$HOME/.PlayOnLinux/wine/linux-x86/"
    ```

    A listagem deve conter `5.8/`.
    
4. Reinicie o `PlayOnLinux` depois de copiar o _runner_.


## 4. Configurar o `PlayOnLinux (POL)` [5]

### 4.1 Passos iniciais

**A considerar:** este procedimento usa o `Wine x86 5.8`. A referência [5] relata que, no guia original, o autor considerou o `Wine x86 4.15` mais estável do que `3.4` ou `3.14`, citando uma postagem de GlasierXplor no fórum do `PlayOnLinux`; a fonte também menciona o `PlayOnLinux 4.3.4` como requisito para o Wine 4.15. Essa comparação é histórica e não avalia o Wine 5.8.

1. A versão `5.8` do `Wine x86` foi usada para esta instalação, então verifique se ele está
instalado iniciando o `PlayOnLinux (POL)` e selecionando `Tools -> Manage Wine versions`. Janela
Gerenciar versões do `Wine` com `x86` versão `5.8` instalada

<div align="center">
    <img src="docs/figures/playonlinux_wine_versions_manager.png" alt="Minha Imagem" />
    <p>Fig. 7. PlayOnLinux wine versions manager.</p>
</div>

2. Se o `Wine x86` versão `5.8` não aparecer em `Installed Wine versions`, selecione-a na janela
`Available Wine versions:` e clique no botão `>` meio da janela para instalá-lo. Depois de
instalado, **feche** e saia para o menu principal do `PlayOnLinux (POL)`.

3. No `PlayOnLinux (POL)`, selecione `Configure` para entrar na tela de configuração e clique `New`
no canto inferior esquerdo para iniciar o criador do _drive_ virtual.

4. Selecione instalação do `Windows` de `32 bits` e pressione `Next`. Jogue no `Linux 32`
instalação do `Windows` de `32 bits`

<div align="center">
    <img src="docs/figures/playonlinux_create_32_bit_virtual_drive.png" alt="Minha Imagem" />
    <p>Fig. 8. PlayOnLinux Wizard .</p>
</div>

5. Selecione `Wine` versão `5.8` e pressione `Next`.

6. Dê um nome ao _drive_ virtual (por exemplo `wine58office2016pp`) e pressione `Next` para iniciar a
criação. Selecione para instalar o `Mono` se o `POL` solicitar.

7. Assim que a criação da unidade virtual for concluída, você deverá retornar à tela principal de
configuração do `PlayOnLinux (POL)`. Certifique-se de que a unidade recém-criada (por exemplo
`wine58office2016pp`) esteja selecionada na janela esquerda.

### 4.2 Instalar componentes

#### 4.2.1 Instalar componentes pelo `PlayOnLinux (POL)`

Depois de executar os passos da Seção anterior, execute:

1. Clique na guia `Install components` na parte superior. Em seguida, role para baixo para
selecionar `msxml6e` clique em `Install`.

<div align="center">
    <img src="docs/figures/playonlinux_install_msxml6_component.png" alt="Minha Imagem" />
    <p>Fig. 9. PLayOnLinux configuration .</p>
</div>

2. **Repita a etapa acima para instalar o(s) componente(s)**: o prefixo ideal deve ter:

    - `dotnet40`

    - `msxml6`

    - `riched20`

    - `vcrun2013`

    - `corefonts`

#### 4.2.2 Instalar os componentes pelo `Terminal Emulator` (recomendado)

Ao invés de instalar os componentes pelo `PlayOnLinux (POL)`, você pode instalar pelo `Terminal Emulator`, como segue:

1. Você pode instalar tudo de uma vez manualmente:

    ```bash
    WINEPREFIX=~/.PlayOnLinux/wineprefix/wine58office2016pp winetricks dotnet40 msxml6 riched20 vcrun2013 corefonts
    ```

    **ATENÇÃO**: Perceba que, se você instalar o ambiente com outra versão do `wine`, você terá que alterar o
    nome de `wine58office2016pp` conforme o nome que você criou, por exemplo, para a versão do
    `wine 3.14` pode ser `wine314office2016pp`.

### 4.3 Passos finais

1. Selecione a guia `Wine` na tela Configuração `PlayOnLinux (POL)` e clique em `Configure Wine`.

2. Assim que a tela Configuração do `Wine` aparecer, clique na guia `Libraries`. Clique em
`Edit...` para alterar `msxml6` e `riched20` para `(native, builtin)` ou `Native then Builtin`.

<div align="center">
    <img src="docs/figures/playonlinux_wine_library_overrides.png" alt="Minha Imagem" />
    <p>Fig. 10. Wine Configuration - Edit override.</p>
</div>

3. Na tela de configuração do `Wine`, clique na aba `Applications` e certifique-se de que
`Windows 7` esteja selecionada como a versão do `Windows`. Saia para a tela de configuração do
`PlayOnLinux (POL)`.

<div align="center">
    <img src="docs/figures/wine_configuration_applications.png" alt="Minha Imagem" />
    <p>Fig. 11. Wine Configuration - Applications.</p>
</div>

4. Selecione a guia `Wine` na tela Configuração `PlayOnLinux (POL)` e clique em `Registry Editor`
para abrir o Editor do Registro.

5. Selecione para `HKEY_CURRENT_USER-> Software-> Wine`

6. Clique `Edit-> New-> Key` e nomeie esta chave `Direct2D`.

7. Selecione `Direct2D` e então `Edit-> New-> DWORD Value` e nomeie para `max_version_factory`
com um valor de `0`.

<div align="center">
    <img src="docs/figures/playonlinux_registry_editor_direct2d.png" alt="Minha Imagem" />
    <p>Fig. 12. Registry Editor .</p>
</div>

8. Feche o `Registry Editor` e retorne à tela Configuração do `PlayOnLinux (POL)`.


## 5. Configurar/Instalar/Usar o `Microsoft Office 2016` no `Linux Ubuntu` (caso ainda não esteja instalado) [1]

Para configurar/instalar/usar o `Microsoft Office 2016` no `Linux Ubuntu`, siga os passos abaixo::

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    
    ```bash
    sudo apt clean
    ``` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: 
    
    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:
    
    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    
    ```bash
    sudo apt clean
    ``` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  
    
    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:
    
    ```bash
    sudo apt full-upgrade -y
    ```

3. **Adicionar os repositórios oficiais do `Linux Ubuntu`**:

    ```bash
    sudo add-apt-repository main -y
    sudo add-apt-repository restricted -y
    sudo add-apt-repository universe -y
    sudo add-apt-repository multiverse -y
    sudo apt update
    ```

    3.1. O instalador de 32 bits precisa da biblioteca gráfica `libGL.so.1` de 32 bits bem como do
    `winbind`. No `Terminal Emulator`, habilite a arquitetura `i386` e instale o pacote:

    ```bash
    sudo dpkg --add-architecture i386
    sudo apt update
    sudo apt install libgl1:i386 -y
    sudo apt install winbind -y
    ```


4. Criar o ponto de montagem `~/office2016pp`, se ele ainda não existir:

    ```bash
    mkdir -pv ~/office2016pp
    ```

5. Montar o arquivo `.ISO` baixado. O comando abaixo monta a imagem dentro da pasta `~/office2016pp`:

    ```bash
    sudo mount -o loop ~/Downloads/SW_DVD5_Office_Professional_Plus_2016_W32_English_MLF_X20-41353.ISO ~/office2016pp
    ```

6. Clicar em `Install a program`:

<div align="center">
    <img src="docs/figures/playonlinux_main_window.png" alt="Minha Imagem" />
    <p>Fig. 13. `Install a program`.</p>
</div>


7. Clicar em `Search`:

<div align="center">
    <img src="docs/figures/playonlinux_install_menu.png" alt="Minha Imagem" />
    <p>Fig. 14. `Search`.</p>
</div>


8. Digitar `Microsoft Office 2016 (method B)`:

<div align="center">
    <img src="docs/figures/playonlinux_search_office_2016.png" alt="Minha Imagem" />
    <p>Fig. 15. `Microsoft Office 2016`.</p>
</div>


9. Clicar em `Microsoft Office 2016 (method B)`:

<div align="center">
    <img src="docs/figures/playonlinux_select_office_2016_method_b.png" alt="Minha Imagem" />
    <p>Fig. 16. `Microsoft Office 2016 (method B)`.</p>
</div>



10. Clicar em `Install`:

<div align="center">
    <img src="docs/figures/playonlinux_method_b_selected.png" alt="Minha Imagem" />
    <p>Fig. 17. `Install`.</p>
</div>


11. Clicar em `Next`:

<div align="center">
    <img src="docs/figures/playonlinux_during_a_playonlinux_installation.png" alt="Minha Imagem" />
    <p>Fig. 18. `PlayOnLinux - During a PlayOnLinux Installation`.</p>
</div>


12. Clicar em `Next`:

<div align="center">
    <img src="docs/figures/playonlinux_is_not_related_to_winehq.png" alt="Minha Imagem" />
    <p>Fig. 19. `PlayOnLinux - PlayOnLinux is not related to WineHQ`.</p>
</div>


13. Clicar em `Use a setup file in my computer` e clicar em `Next`:

<div align="center">
    <img src="docs/figures/playonlinux_please_choose_an_installation_method.png" alt="Minha Imagem" />
    <p>Fig. 20. `PlayOnLinux - Please choose an installation method`.</p>
</div>


14. Clicar em `Browse`:

<div align="center">
    <img src="docs/figures/playonlinux_please_select_the_setup_file_to_run.png" alt="Minha Imagem" />
    <p>Fig. 21. `PlayOnLinux - Please select the setup file to run`.</p>
</div>


15. Na janela de arquivos, abrir o ponto de montagem `~/office2016`, selecionar o arquivo `setup.exe` que está dentro dele e clicar em `Open`; em seguida, clicar em `Next`. Selecione o `setup.exe`, não o arquivo `.ISO` inteiro:

<div align="center">
    <img src="docs/figures/playonlinux_select_setup_exe_from_mounted_iso.png" alt="Minha Imagem" />
    <p>Fig. 22. Arquivo setup.exe selecionado no ponto de montagem.</p>
</div>

16. Clicar em `Next`:

<div align="center">
    <img src="docs/figures/playonlinux_the_wizard_will_help_you_install_microsoft_office_2016_on_your_computer.png" alt="Minha Imagem" />
    <p>Fig. 23. `PlayOnLinux - Welcome to PlayOnLinux Installation Wizard`.</p>
</div>


17. Seguir as instruções do instalador do Office.

<div align="center">
    <img src="docs/figures/office_2016_installer_window.png" alt="Minha Imagem" />
    <p>Fig. 24. Instalador do `Microsoft Office 2016`.</p>
</div>


## Referências

[1] OPENAI.
**Instalar o `microsoft office 2016` no `linux ubuntu` pelo `terminal emulator`.**
Disponível em: <https://chat.openai.com/c/f4373ad1-fde7-48c6-933a-91a70564cb26> (texto adaptado).
ChatGPT.
Acessado em: 05/11/2023 23:22.

[2] OPENAI.
**Instalar o `bottles` no `linux ubuntu` pelo `terminal emulator`.**
Disponível em: <https://chat.openai.com/c/92444ccc-f995-4e9c-8f03-678931882241> (texto adaptado).
ChatGPT.
Acessado em: 01/11/2023 19:17.

[3] OPENAI.
**Extrair iso com 7-zip.**
Disponível em: <https://chat.openai.com/c/9aeb16fc-d4dc-4a5b-a7eb-cd82d851d7b7> (texto adaptado).
ChatGPT.
Acessado em: 06/11/2023 09:37.

[4] OPENAI.
**Converter arquivo `.iso` em `.img`.**
Disponível em: <https://chat.openai.com/c/498fa917-4067-4fc5-b69d-31c9514dc47e> (texto adaptado).
ChatGPT.
Acessado em: 23/11/2023 13:47.

[5] ASK UBUNTU (STACK EXCHANGE).
**How do I install MS Office 2016 on PlayOnLinux?**
Disponível em: <https://askubuntu.com/questions/975104/how-do-i-install-ms-office-2016-on-playonlinux>.
Acessado em: 02/10/2026.

