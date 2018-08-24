---
title: Obter a ID do projeto em uma parte do suplemento em uma página de Detalhes do Projeto
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Suplemento partes são hospedados nos elementos iframe que estejam totalmente isolados da página de hospedagem. Para obter informações sobre o projeto atual de uma parte suplemento na página de detalhes do projeto (PDP), você pode usar o método window.postMessage, um ouvinte de eventos e um manipulador de eventos que analisa os a ID do projeto da mensagem.
ms.openlocfilehash: d9f6d02f328860f46784f86c049581fa28bb4749
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594422"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Obter a ID do projeto em uma parte do suplemento em uma página de Detalhes do Projeto

Suplemento partes são hospedados nos elementos **iframe** que estejam totalmente isolados da página de hospedagem. Para obter informações sobre o projeto atual de uma parte suplemento na página de detalhes do projeto (PDP), você pode usar o método **window.postMessage** , um ouvinte de eventos e um manipulador de eventos que analisa os a ID do projeto da mensagem. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Pré-requisitos para a criação de uma hospedado no SharePoint suplemento part que obtém a ID do projeto
<a name="Prereqs"> </a>

Para usar o exemplo de código neste artigo, você precisará um destes procedimentos:
  
- SharePoint 2013 e Project Server 2013, configurados para o isolamento do suplemento. Se você estiver desenvolvendo remotamente, o servidor deve suportar sideloading de suplementos ou você deve instalar o suplemento em um Site do desenvolvedor.
  
- SharePoint Online e Project Online
    
    - Visual Studio 2013, o Visual Studio 2012 no Office Developer Tools para Visual Studio 2013 ou Napa
        
    - Permissões suficientes para o usuário conectado:
        
        - Permissões de administrador local no computador de desenvolvimento.
            
        - Acesso de leitura pelo menos um projeto.
            
        - Permissão para editar páginas no site do Project Web App.
            
        - Você deve estar conectado como alguém que não seja a conta do sistema. A conta do sistema não tem permissão para instalar um suplemento.
    
Consulte [pré-requisitos para a criação de um suplemento do Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) para obter mais informações sobre suplementos para o projeto. Consulte [Configurar um ambiente de desenvolvimento para o SharePoint Add-ins do local](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) para obter orientação sobre a instalação local (incluindo como desabilitar a verificação de loopback, se necessário). Se você estiver desenvolvendo remotamente, consulte [Developing apps for SharePoint em um sistema remoto](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Criar hospedado no SharePoint add-in e o cliente web part
<a name="CreateApp"> </a>

1. Abra o Visual Studio e escolha **arquivo** > **New** > **Project**.
    
2. Na caixa de diálogo **Novo projeto**, escolha o **.NET Framework 4.5** da lista suspensa na parte superior da caixa de diálogo. 
    
3. Na lista de **modelos** , escolha **Visual c#** > **Office/SharePoint** > **suplementos** > **suplemento para o SharePoint 2013**.
    
4. Nomeie o suplemento GetProjectIdAddinPart e escolha o botão **Okey** . 
    
5. Na caixa de diálogo **novo suplemento para o SharePoint** , insira a URL do site do PWA que você deseja usar para depuração (por exemplo: _https://contoso.com/sites/pwasite/_).
    
6. Escolha a opção **hospedado no SharePoint** para hospedar o add-in e, em seguida, escolha o botão **Concluir** . 
    
7. No **Solution Explorer**, abra o menu de atalho para o projeto GetProjectIdAddinPart e escolha **Adicionar** > **Novo Item**.
    
8. Na caixa de diálogo **Adicionar Novo Item** , escolha **cliente web part (Host Web)**, nomeie a web part GetProjectId e escolha o botão **Adicionar** . 
    
9. Na caixa de diálogo **Criar cliente da web part** , escolha a opção **criar uma nova página da web part cliente** e escolha o botão **Concluir** . 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Obter a ID do projeto na parte suplemento
<a name="GetProjectId"> </a>

A parte de suplemento de GetProjectId define seu código personalizado na página da web part cliente GetProjectId.aspx. A lógica que recebe e processa a mensagem é definida no elemento **cabeça** da página e os controles de página são definidos no elemento **body** da página. 
  
1. Abra a página de web parts GetProjectId.aspx (na pasta **páginas** ). 
    
2. No elemento **cabeça** da página, substitua o código entre as marcas de **script** com o código a seguir. 
    
   ```js
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
                (function () {
                    var hostUrl = '';
                    var link = document.createElement('link');
                    link.setAttribute('rel', 'stylesheet');
                    if (document.URL.indexOf('?') != -1) {
                        var params = document.URL.split('?')[1].split('&');
                        for (var i = 0; i < params.length; i++) {
                            var p = decodeURIComponent(params[i]);
                            if (/^SPHostUrl=/i.test(p)) {
                                hostUrl = p.split('=')[1];
                                link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                                break;
                            }
                        }
                    }
                    if (hostUrl == '') {
                        link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
                    }
                    document.head.appendChild(link);
                })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
   ```

3. Adicione o seguinte código no elemento **body** da página. O código define um controle de intervalo que exibe a ID do projeto. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. No arquivo Elements. XML, opcionalmente, altere o nome, título, descrição e o tamanho padrão da parte add-in. Este exemplo usa os valores padrão.
    
5. Para testar a parte suplemento, na barra de menus, escolha **Depurar**, **Iniciar depuração**. Se você for solicitado para modificar o arquivo Web. config, escolha o botão de **Okey** . 
    
   Para depurar a parte do suplemento, definir pontos de interrupção apropriados no script que você adicionou.
    
6. Navegue até uma página PDP e escolha **Editar página** no menu Ferramentas (ícone de engrenagem). 
    
7. Adicione a parte do **Título do GetProjectId** a uma web part na página. A ID do projeto exibe **estendem** controle na página de web Parts. 
    
## <a name="next-steps"></a>Próximas etapas
<a name="NextSteps"> </a>

A parte de suplemento neste exemplo não acessar dados do Project Server ou dados do SharePoint. Você pode usar a identificação do produto para obter mais informações sobre o projeto atual usando um cliente API, como o modelo de objeto JavaScript ou o serviço REST.
  
No arquivo AppManifest.xml, especifique as permissões que seu suplemento precisa acessar dados do Project Server ou os dados do SharePoint. 
  
Consulte [Criar Suplemento partes para instalar com o suplemento do SharePoint](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) para aprender a definir propriedades personalizadas de uma parte do suplemento. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Exemplo: Obtendo a ID do projeto em uma parte add-in em uma página PDP
<a name="CodeExample"> </a>

O exemplo a seguir é o código completo em página de GetProjectID.aspx do cliente da web part. O código registra um ouvinte de eventos e um manipulador de eventos que recebe e analisa uma mensagem que contém a ID do projeto.
  
```HTML
<%@ Page language="C#" Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<WebPartPages:AllowFraming ID="AllowFraming" runat="server" />
<html>
<head>
    <title></title>
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/MicrosoftAjax.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.js"></script>
    <script type="text/javascript">
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
        (function () {
            var hostUrl = '';
            var link = document.createElement('link');
            link.setAttribute('rel', 'stylesheet');
            if (document.URL.indexOf('?') != -1) {
                var params = document.URL.split('?')[1].split('&');
                for (var i = 0; i < params.length; i++) {
                    var p = decodeURIComponent(params[i]);
                    if (/^SPHostUrl=/i.test(p)) {
                        hostUrl = p.split('=')[1];
                        link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                        break;
                    }
                }
            }
            if (hostUrl == '') {
                link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
            }
            document.head.appendChild(link);
        })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
    </script>
</head>
<body>
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
</body>
</html>

```

## <a name="see-also"></a>Confira também

- [Tarefas de programação do Project](project-programming-tasks.md)
- [Criar um suplemento do Project Server hospedado pelo SharePoint](create-a-sharepoint-hosted-project-server-add-in.md)
- [Criar partes de suplementos para instalação com o seu Suplemento do SharePoint](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

