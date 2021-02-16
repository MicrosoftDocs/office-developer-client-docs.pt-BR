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
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="7ec3e-104">Obter a ID do projeto em uma parte do suplemento em uma página de Detalhes do Projeto</span><span class="sxs-lookup"><span data-stu-id="7ec3e-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="7ec3e-105">As partes do complemento são hospedadas em elementos **iframe** que são totalmente isolados da página de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="7ec3e-106">Para obter informações sobre o projeto atual a partir de uma parte de um add-in na Página de Detalhes do Projeto (PDP), você pode usar o método **window.postMessage,** um ouvinte de eventos e um manipulador de eventos que analisará a ID do projeto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="7ec3e-107">Pré-requisitos para criar uma parte do add-in hospedado no SharePoint que obtém a ID do projeto</span><span class="sxs-lookup"><span data-stu-id="7ec3e-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="7ec3e-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="7ec3e-108"><a name="Prereqs"> </a></span></span>

<span data-ttu-id="7ec3e-109">Para usar o exemplo de código neste artigo, você precisará de um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="7ec3e-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="7ec3e-110">SharePoint 2013 e Project Server 2013, configurados para isolamento de add-in.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="7ec3e-111">Se você estiver desenvolvendo remotamente, o servidor deve dar suporte ao sideload de complementos ou você deve instalar o complemento em um Site do Desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="7ec3e-112">SharePoint Online e Project Online</span><span class="sxs-lookup"><span data-stu-id="7ec3e-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="7ec3e-113">Visual Studio 2013, Visual Studio 2012 com Office Developer Tools para Visual Studio 2013 ou Napa</span><span class="sxs-lookup"><span data-stu-id="7ec3e-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="7ec3e-114">Permissões suficientes para o usuário conectado:</span><span class="sxs-lookup"><span data-stu-id="7ec3e-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="7ec3e-115">Permissões de administrador local no computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="7ec3e-116">Acesso de leitura a pelo menos um projeto.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="7ec3e-117">Permissão para editar páginas no site do Project Web App.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="7ec3e-118">Você deve estar conectado como alguém que não seja a conta do sistema.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="7ec3e-119">A conta do sistema não tem permissão para instalar um complemento.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="7ec3e-120">Consulte Pré-requisitos para criar um complemento para [o Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) para obter mais informações sobre os complementos do Project.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="7ec3e-121">Confira Configurar um ambiente de desenvolvimento local para Os Complementos do [SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) para obter orientação sobre a instalação local (incluindo como desabilitar a verificação de loopback, se necessário).</span><span class="sxs-lookup"><span data-stu-id="7ec3e-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="7ec3e-122">Se você estiver desenvolvendo remotamente, consulte [Desenvolvendo aplicativos para SharePoint em um sistema remoto.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)</span><span class="sxs-lookup"><span data-stu-id="7ec3e-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="7ec3e-123">Criar o web part do cliente e o complemento hospedado pelo SharePoint</span><span class="sxs-lookup"><span data-stu-id="7ec3e-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="7ec3e-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="7ec3e-124"><a name="CreateApp"> </a></span></span>

1. <span data-ttu-id="7ec3e-125">Abra o Visual Studio e escolha **Arquivo**  >  **Novo**  >  **Projeto.**</span><span class="sxs-lookup"><span data-stu-id="7ec3e-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="7ec3e-126">Na caixa de diálogo **Novo Projeto**, escolha **.NET Framework 4.5** na lista suspensa na parte superior da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="7ec3e-127">Na lista **de modelos,** escolha **Visual C#**  >  **Office/SharePoint**  >  **Add-ins**  >  **Add-ins for SharePoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="7ec3e-128">Nome do complemento GetProjectIdAddinPart e escolha o **botão OK.**</span><span class="sxs-lookup"><span data-stu-id="7ec3e-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="7ec3e-129">Na caixa de diálogo Novo complemento para **SharePoint,** insira a URL do site do PWA que você deseja usar para depuração (por exemplo:  _https://contoso.com/sites/pwasite/_ ).</span><span class="sxs-lookup"><span data-stu-id="7ec3e-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="7ec3e-130">Escolha a **opção hospedada pelo SharePoint** para hospedar seu complemento e, em seguida, escolha o **botão** Concluir.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="7ec3e-131">No **Solution Explorer,** abra o menu de atalho do projeto GetProjectIdAddinPart e escolha **Adicionar**  >  **Novo Item.**</span><span class="sxs-lookup"><span data-stu-id="7ec3e-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="7ec3e-132">In the **Add New Item** dialog box, choose Client web part **(Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="7ec3e-133">Na caixa **de diálogo Criar Web Part** do Cliente, escolha a opção Criar uma nova página de Web **Part** do cliente e, em seguida, escolha o **botão** Concluir.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="7ec3e-134">Obter a ID do projeto na parte do complemento</span><span class="sxs-lookup"><span data-stu-id="7ec3e-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="7ec3e-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="7ec3e-135"><a name="GetProjectId"> </a></span></span>

<span data-ttu-id="7ec3e-136">A parte do complemento GetProjectId define seu código personalizado na página GetProjectId.aspx da Web Part do cliente.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="7ec3e-137">A lógica que recebe e lida com a mensagem é definida no elemento **head** da página e os controles de página são definidos no elemento **body** da página.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="7ec3e-138">Abra a página da Web Part GetProjectId.aspx (na **pasta** Páginas).</span><span class="sxs-lookup"><span data-stu-id="7ec3e-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="7ec3e-139">No elemento **head** da página, substitua o código entre as marcas **de script** pelo código a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
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

3. <span data-ttu-id="7ec3e-140">Adicione o código a seguir no **elemento body** da página.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="7ec3e-141">O código define um controle span que exibe a ID do projeto.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="7ec3e-142">No arquivo Elements.xml, opcionalmente, altere o nome, o título, a descrição e o tamanho padrão da parte do complemento.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="7ec3e-143">Este exemplo usa os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="7ec3e-144">Para testar a parte do complemento, na barra de menus, escolha **Depurar,** **Iniciar Depuração.**</span><span class="sxs-lookup"><span data-stu-id="7ec3e-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="7ec3e-145">Se você for solicitado a modificar o arquivo web.config, escolha o **botão OK.**</span><span class="sxs-lookup"><span data-stu-id="7ec3e-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="7ec3e-146">Para depurar a parte do complemento, de definir pontos de interrupção apropriados no script que você adicionou.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="7ec3e-147">Navegue até uma página PDP e escolha **Editar página** no menu Ferramentas (ícone de engrenagem).</span><span class="sxs-lookup"><span data-stu-id="7ec3e-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="7ec3e-148">Adicione a **parte Título de GetProjectId** a uma Web Part na página.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="7ec3e-149">A ID do projeto é exibida no controle **span** na página da Web Part.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="7ec3e-150">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="7ec3e-150">Next steps</span></span>
<span data-ttu-id="7ec3e-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="7ec3e-151"><a name="NextSteps"> </a></span></span>

<span data-ttu-id="7ec3e-152">A parte do complemento neste exemplo não acessa dados do Project Server ou dados do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="7ec3e-153">Você pode usar a ID do produto (Product ID) para obter informações sobre o projeto atual usando uma API do cliente, como o modelo de objeto JavaScript ou o serviço REST.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="7ec3e-154">No arquivo AppManifest.xml, especifique as permissões que seu add-in precisa para acessar dados do Project Server ou dados do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="7ec3e-155">Confira [Criar partes de add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) para instalar com o seu Add-in do SharePoint para saber como definir propriedades personalizadas para uma parte de um complemento.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-155">See [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="7ec3e-156">Exemplo: Obter a ID do projeto em uma parte de um complemento em uma página PDP</span><span class="sxs-lookup"><span data-stu-id="7ec3e-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="7ec3e-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="7ec3e-157"><a name="CodeExample"> </a></span></span>

<span data-ttu-id="7ec3e-158">O exemplo a seguir é o código completo na página GetProjectID.aspx da Web Part do cliente.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="7ec3e-159">O código registra um ouvinte de eventos e um manipulador de eventos que recebe e analisado uma mensagem que contém a ID do projeto.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="7ec3e-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ec3e-160">See also</span></span>

- [<span data-ttu-id="7ec3e-161">Tarefas de programação do Project</span><span class="sxs-lookup"><span data-stu-id="7ec3e-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="7ec3e-162">Criar um suplemento do Project Server hospedado pelo SharePoint</span><span class="sxs-lookup"><span data-stu-id="7ec3e-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="7ec3e-163">Criar partes de suplementos para instalação com o seu Suplemento do SharePoint</span><span class="sxs-lookup"><span data-stu-id="7ec3e-163">Create add-in parts to install with your SharePoint Add-in</span></span>](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

