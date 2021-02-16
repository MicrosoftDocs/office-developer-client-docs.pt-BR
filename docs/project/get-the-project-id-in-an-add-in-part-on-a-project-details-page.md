---
title: Obter a ID do projeto em uma parte do suplemento em uma página de Detalhes do Projeto
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: As partes do complemento são hospedadas em elementos de iframe que são totalmente isolados da página de hospedagem. Para obter informações sobre o projeto atual a partir de uma parte de um add-in na Página de Detalhes do Projeto (PDP), você pode usar o método window.postMessage, um ouvinte de eventos e um manipulador de eventos que analisará a ID do projeto da mensagem.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322593"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Obter a ID do projeto em uma parte do suplemento em uma página de Detalhes do Projeto

As partes do complemento são hospedadas em elementos **iframe** que são totalmente isolados da página de hospedagem. Para obter informações sobre o projeto atual a partir de uma parte de um add-in na Página de Detalhes do Projeto (PDP), você pode usar o método **window.postMessage,** um ouvinte de eventos e um manipulador de eventos que analisará a ID do projeto da mensagem. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Pré-requisitos para criar uma parte do add-in hospedado no SharePoint que obtém a ID do projeto
<a name="Prereqs"> </a>

Para usar o exemplo de código neste artigo, você precisará de um dos seguintes:
  
- SharePoint 2013 e Project Server 2013, configurados para isolamento de add-in. Se você estiver desenvolvendo remotamente, o servidor deve dar suporte ao sideload de complementos ou você deve instalar o complemento em um Site do Desenvolvedor.
  
- SharePoint Online e Project Online
    
    - Visual Studio 2013, Visual Studio 2012 com Office Developer Tools para Visual Studio 2013 ou Napa
        
    - Permissões suficientes para o usuário conectado:
        
        - Permissões de administrador local no computador de desenvolvimento.
            
        - Acesso de leitura a pelo menos um projeto.
            
        - Permissão para editar páginas no site do Project Web App.
            
        - Você deve estar conectado como alguém que não seja a conta do sistema. A conta do sistema não tem permissão para instalar um complemento.
    
Consulte Pré-requisitos para criar um complemento para [o Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) para obter mais informações sobre os complementos do Project. Confira Configurar um ambiente de desenvolvimento local para Os Complementos do [SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) para obter orientação sobre a instalação local (incluindo como desabilitar a verificação de loopback, se necessário). Se você estiver desenvolvendo remotamente, consulte [Desenvolvendo aplicativos para SharePoint em um sistema remoto.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Criar o web part do cliente e o complemento hospedado pelo SharePoint
<a name="CreateApp"> </a>

1. Abra o Visual Studio e escolha **Arquivo**  >  **Novo**  >  **Projeto.**
    
2. Na caixa de diálogo **Novo Projeto**, escolha **.NET Framework 4.5** na lista suspensa na parte superior da caixa de diálogo. 
    
3. Na lista **de modelos,** escolha **Visual C#**  >  **Office/SharePoint**  >  **Add-ins**  >  **Add-ins for SharePoint 2013**.
    
4. Nome do complemento GetProjectIdAddinPart e escolha o **botão OK.** 
    
5. Na caixa de diálogo Novo complemento para **SharePoint,** insira a URL do site do PWA que você deseja usar para depuração (por exemplo:  _https://contoso.com/sites/pwasite/_ ).
    
6. Escolha a **opção hospedada pelo SharePoint** para hospedar seu complemento e, em seguida, escolha o **botão** Concluir. 
    
7. No **Solution Explorer,** abra o menu de atalho do projeto GetProjectIdAddinPart e escolha **Adicionar**  >  **Novo Item.**
    
8. In the **Add New Item** dialog box, choose Client web part **(Host Web)**, name the web part GetProjectId, and then choose the **Add** button. 
    
9. Na caixa **de diálogo Criar Web Part** do Cliente, escolha a opção Criar uma nova página de Web **Part** do cliente e, em seguida, escolha o **botão** Concluir. 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Obter a ID do projeto na parte do complemento
<a name="GetProjectId"> </a>

A parte do complemento GetProjectId define seu código personalizado na página GetProjectId.aspx da Web Part do cliente. A lógica que recebe e lida com a mensagem é definida no elemento **head** da página e os controles de página são definidos no elemento **body** da página. 
  
1. Abra a página da Web Part GetProjectId.aspx (na **pasta** Páginas). 
    
2. No elemento **head** da página, substitua o código entre as marcas **de script** pelo código a seguir. 
    
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

3. Adicione o código a seguir no **elemento body** da página. O código define um controle span que exibe a ID do projeto. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. No arquivo Elements.xml, opcionalmente, altere o nome, o título, a descrição e o tamanho padrão da parte do complemento. Este exemplo usa os valores padrão.
    
5. Para testar a parte do complemento, na barra de menus, escolha **Depurar,** **Iniciar Depuração.** Se você for solicitado a modificar o arquivo web.config, escolha o **botão OK.** 
    
   Para depurar a parte do complemento, de definir pontos de interrupção apropriados no script que você adicionou.
    
6. Navegue até uma página PDP e escolha **Editar página** no menu Ferramentas (ícone de engrenagem). 
    
7. Adicione a **parte Título de GetProjectId** a uma Web Part na página. A ID do projeto é exibida no controle **span** na página da Web Part. 
    
## <a name="next-steps"></a>Próximas etapas
<a name="NextSteps"> </a>

A parte do complemento neste exemplo não acessa dados do Project Server ou dados do SharePoint. Você pode usar a ID do produto (Product ID) para obter informações sobre o projeto atual usando uma API do cliente, como o modelo de objeto JavaScript ou o serviço REST.
  
No arquivo AppManifest.xml, especifique as permissões que seu add-in precisa para acessar dados do Project Server ou dados do SharePoint. 
  
Confira [Criar partes de add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) para instalar com o seu Add-in do SharePoint para saber como definir propriedades personalizadas para uma parte de um complemento. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Exemplo: Obter a ID do projeto em uma parte de um complemento em uma página PDP
<a name="CodeExample"> </a>

O exemplo a seguir é o código completo na página GetProjectID.aspx da Web Part do cliente. O código registra um ouvinte de eventos e um manipulador de eventos que recebe e analisado uma mensagem que contém a ID do projeto.
  
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
- [Criar partes de suplementos para instalação com o seu Suplemento do SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

