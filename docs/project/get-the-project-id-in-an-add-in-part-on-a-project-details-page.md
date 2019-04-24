---
title: Obter a ID do projeto em uma parte do suplemento em uma página de Detalhes do Projeto
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Partes de suplemento são hospedadas em elementos iframe totalmente isolados da página de hospedagem. Para obter informações sobre o projeto atual de uma parte de suplemento na página de detalhes do projeto (PDP), você pode usar o método window. isMessage, um ouvinte de evento e um manipulador de eventos que analisa a ID do projeto da mensagem.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322593"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Obter a ID do projeto em uma parte do suplemento em uma página de Detalhes do Projeto

Partes de suplemento são hospedadas em elementos **iframe** totalmente isolados da página de hospedagem. Para obter informações sobre o projeto atual de uma parte de suplemento na página de detalhes do projeto (PDP), você pode usar o método **Window. ismessage** , um ouvinte de evento e um manipulador de eventos que analisa a ID do projeto da mensagem. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Pré-requisitos para a criação de uma parte de suplemento hospedado pelo SharePoint que obtém a ID do projeto
<a name="Prereqs"> </a>

Para usar o exemplo de código neste artigo, você precisará de um dos seguintes:
  
- SharePoint 2013 e Project Server 2013, configurado para isolamento de suplemento. Se você estiver desenvolvendo remotamente, o servidor deve oferecer suporte ao Sideload de suplementos ou você deve instalar o suplemento em um site do desenvolvedor.
  
- SharePoint Online e Project online
    
    - Visual Studio 2013, Visual Studio 2012 com Office Developer Tools para Visual Studio 2013 ou Napa
        
    - Permissões suficientes para o usuário conectado:
        
        - Permissões de administrador local no computador de desenvolvimento.
            
        - Acesso de leitura a pelo menos um projeto.
            
        - Permissão para editar páginas no site do Project Web App.
            
        - Você deve estar conectado como alguém que não seja a conta do sistema. A conta do sistema não tem permissão para instalar um suplemento.
    
Consulte [pré-requisitos para criar um suplemento para o Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) para obter mais informações sobre os suplementos do Project. ConFira [configurar um ambiente de desenvolvimento local para](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) suplementos do SharePoint para obter orientação sobre a instalação local (incluindo como desabilitar a verificação de auto-retorno, se necessário). Se você estiver desenvolvendo remotamente, consulte [desenvolvendo aplicativos para SharePoint em um sistema remoto](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Criar o suplemento hospedado pelo SharePoint e a Web Part do cliente
<a name="CreateApp"> </a>

1. Abra o Visual Studio e escolha **arquivo** > **novo** > **projeto**.
    
2. Na caixa de diálogo **Novo projeto**, escolha o **.NET Framework 4.5** da lista suspensa na parte superior da caixa de diálogo. 
    
3. na lista **de modelos** , escolha suplemento do **Visual C#** > **Office/sharepoint** > **add-ins** > **para o SharePoint 2013**.
    
4. Nomeie o suplemento GetProjectIdAddinPart e, em seguida, escolha o botão **OK** . 
    
5. Na caixa de diálogo **novo suplemento para SharePoint** , digite a URL do site do PWA que você deseja usar para depuração (por exemplo: _https://contoso.com/sites/pwasite/_).
    
6. Escolha a opção **hospedado pelo SharePoint** para hospedar seu suplemento e, em seguida, escolha o botão **concluir** . 
    
7. No **Gerenciador de soluções**, abra o menu de atalho para o projeto GetProjectIdAddinPart e escolha **Adicionar** > **novo item**.
    
8. Na caixa de diálogo **Adicionar novo item** , escolha **cliente Web Part (host da Web)**, nomeie a Web Part getprojectid e, em seguida, escolha o botão **Adicionar** . 
    
9. Na caixa de diálogo **criar Web Part do cliente** , escolha a opção **criar uma nova página de Web Parts de cliente** e, em seguida, escolha o botão **concluir** . 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Obter a ID do projeto na parte do suplemento
<a name="GetProjectId"> </a>

A parte do suplemento getProjectid define o código personalizado na página getProjectid. aspx da Web Part cliente. A lógica que recebe e manipula a mensagem é definida no elemento **Head** da página e os controles de página são definidos no elemento **Body** da página. 
  
1. Abra a página de Web Part getProjectid. aspx (na pasta **páginas** ). 
    
2. No elemento **Head** da página, substitua o código entre as marcas de **script** com o código a seguir. 
    
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

3. Adicione o seguinte código no elemento **Body** da página. O código define um controle span que exibe a ID do projeto. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. No arquivo elements. xml, altere opcionalmente o nome, o título, a descrição e o tamanho padrão da parte do suplemento. Este exemplo usa os valores padrão.
    
5. Para testar a parte do suplemento, na barra de menus, escolha **depurar**, **Iniciar Depuração**. Se você for solicitado a modificar o arquivo Web. config, escolha o botão **OK** . 
    
   Para depurar a parte do suplemento, defina pontos de interrupção apropriados no script que você adicionou.
    
6. Navegue até uma página PDP e escolha **Editar página** no menu ferramentas (ícone de engrenagem). 
    
7. Adicione a parte de **título** getprojectid a uma Web Part na página. A ID do projeto é exibida no controle de **span** na página de Web Parts. 
    
## <a name="next-steps"></a>Próximas etapas
<a name="NextSteps"> </a>

A parte do suplemento neste exemplo não acessa dados do Project Server ou dados do SharePoint. Você pode usar a ID do produto para obter informações sobre o projeto atual usando uma API do cliente, como o modelo de objeto do JavaScript ou o serviço REST.
  
No arquivo arquivo AppManifest. xml, especifique as permissões que seu suplemento precisa para acessar dados do Project Server ou dados do SharePoint. 
  
ConFira [criar partes de suplemento para instalar com seu suplemento do SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) para saber como definir propriedades personalizadas para uma parte de suplemento. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Exemplo: obtendo a ID do projeto em uma parte de suplemento em uma página PDP
<a name="CodeExample"> </a>

O exemplo a seguir é o código completo na página getProjectid. aspx da Web Part do cliente. O código registra um ouvinte de evento e um manipulador de eventos que recebe e analisa uma mensagem que contém a ID do projeto.
  
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
- [Criar partes de suplementos para instalação com o seu suplemento do SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

