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
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="3caca-104">Obter a ID do projeto em uma parte do suplemento em uma página de Detalhes do Projeto</span><span class="sxs-lookup"><span data-stu-id="3caca-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="3caca-105">Suplemento partes são hospedados nos elementos **iframe** que estejam totalmente isolados da página de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="3caca-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="3caca-106">Para obter informações sobre o projeto atual de uma parte suplemento na página de detalhes do projeto (PDP), você pode usar o método **window.postMessage** , um ouvinte de eventos e um manipulador de eventos que analisa os a ID do projeto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="3caca-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="3caca-107">Pré-requisitos para a criação de uma hospedado no SharePoint suplemento part que obtém a ID do projeto</span><span class="sxs-lookup"><span data-stu-id="3caca-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="3caca-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="3caca-108"></span></span>

<span data-ttu-id="3caca-109">Para usar o exemplo de código neste artigo, você precisará um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="3caca-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="3caca-110">SharePoint 2013 e Project Server 2013, configurados para o isolamento do suplemento.</span><span class="sxs-lookup"><span data-stu-id="3caca-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="3caca-111">Se você estiver desenvolvendo remotamente, o servidor deve suportar sideloading de suplementos ou você deve instalar o suplemento em um Site do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="3caca-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="3caca-112">SharePoint Online e Project Online</span><span class="sxs-lookup"><span data-stu-id="3caca-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="3caca-113">Visual Studio 2013, o Visual Studio 2012 no Office Developer Tools para Visual Studio 2013 ou Napa</span><span class="sxs-lookup"><span data-stu-id="3caca-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="3caca-114">Permissões suficientes para o usuário conectado:</span><span class="sxs-lookup"><span data-stu-id="3caca-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="3caca-115">Permissões de administrador local no computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="3caca-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="3caca-116">Acesso de leitura pelo menos um projeto.</span><span class="sxs-lookup"><span data-stu-id="3caca-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="3caca-117">Permissão para editar páginas no site do Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3caca-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="3caca-118">Você deve estar conectado como alguém que não seja a conta do sistema.</span><span class="sxs-lookup"><span data-stu-id="3caca-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="3caca-119">A conta do sistema não tem permissão para instalar um suplemento.</span><span class="sxs-lookup"><span data-stu-id="3caca-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="3caca-120">Consulte [pré-requisitos para a criação de um suplemento do Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) para obter mais informações sobre suplementos para o projeto.</span><span class="sxs-lookup"><span data-stu-id="3caca-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="3caca-121">Consulte [Configurar um ambiente de desenvolvimento para o SharePoint Add-ins do local](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) para obter orientação sobre a instalação local (incluindo como desabilitar a verificação de loopback, se necessário).</span><span class="sxs-lookup"><span data-stu-id="3caca-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="3caca-122">Se você estiver desenvolvendo remotamente, consulte [Developing apps for SharePoint em um sistema remoto](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="3caca-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/en-us/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="3caca-123">Criar hospedado no SharePoint add-in e o cliente web part</span><span class="sxs-lookup"><span data-stu-id="3caca-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="3caca-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="3caca-124"></span></span>

1. <span data-ttu-id="3caca-125">Abra o Visual Studio e escolha **arquivo** > **New** > **Project**.</span><span class="sxs-lookup"><span data-stu-id="3caca-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="3caca-126">Na caixa de diálogo **Novo projeto**, escolha o **.NET Framework 4.5** da lista suspensa na parte superior da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3caca-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="3caca-127">Na lista de **modelos** , escolha **Visual c#** > **Office/SharePoint** > **suplementos** > **suplemento para o SharePoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="3caca-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="3caca-128">Nomeie o suplemento GetProjectIdAddinPart e escolha o botão **Okey** .</span><span class="sxs-lookup"><span data-stu-id="3caca-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="3caca-129">Na caixa de diálogo **novo suplemento para o SharePoint** , insira a URL do site do PWA que você deseja usar para depuração (por exemplo: _https://contoso.com/sites/pwasite/_).</span><span class="sxs-lookup"><span data-stu-id="3caca-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="3caca-130">Escolha a opção **hospedado no SharePoint** para hospedar o add-in e, em seguida, escolha o botão **Concluir** .</span><span class="sxs-lookup"><span data-stu-id="3caca-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="3caca-131">No **Solution Explorer**, abra o menu de atalho para o projeto GetProjectIdAddinPart e escolha **Adicionar** > **Novo Item**.</span><span class="sxs-lookup"><span data-stu-id="3caca-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="3caca-132">Na caixa de diálogo **Adicionar Novo Item** , escolha **cliente web part (Host Web)**, nomeie a web part GetProjectId e escolha o botão **Adicionar** .</span><span class="sxs-lookup"><span data-stu-id="3caca-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="3caca-133">Na caixa de diálogo **Criar cliente da web part** , escolha a opção **criar uma nova página da web part cliente** e escolha o botão **Concluir** .</span><span class="sxs-lookup"><span data-stu-id="3caca-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="3caca-134">Obter a ID do projeto na parte suplemento</span><span class="sxs-lookup"><span data-stu-id="3caca-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="3caca-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="3caca-135"></span></span>

<span data-ttu-id="3caca-136">A parte de suplemento de GetProjectId define seu código personalizado na página da web part cliente GetProjectId.aspx.</span><span class="sxs-lookup"><span data-stu-id="3caca-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="3caca-137">A lógica que recebe e processa a mensagem é definida no elemento **cabeça** da página e os controles de página são definidos no elemento **body** da página.</span><span class="sxs-lookup"><span data-stu-id="3caca-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="3caca-138">Abra a página de web parts GetProjectId.aspx (na pasta **páginas** ).</span><span class="sxs-lookup"><span data-stu-id="3caca-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="3caca-139">No elemento **cabeça** da página, substitua o código entre as marcas de **script** com o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="3caca-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
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

3. <span data-ttu-id="3caca-140">Adicione o seguinte código no elemento **body** da página.</span><span class="sxs-lookup"><span data-stu-id="3caca-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="3caca-141">O código define um controle de intervalo que exibe a ID do projeto.</span><span class="sxs-lookup"><span data-stu-id="3caca-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="3caca-142">No arquivo Elements. XML, opcionalmente, altere o nome, título, descrição e o tamanho padrão da parte add-in.</span><span class="sxs-lookup"><span data-stu-id="3caca-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="3caca-143">Este exemplo usa os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="3caca-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="3caca-144">Para testar a parte suplemento, na barra de menus, escolha **Depurar**, **Iniciar depuração**.</span><span class="sxs-lookup"><span data-stu-id="3caca-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="3caca-145">Se você for solicitado para modificar o arquivo Web. config, escolha o botão de **Okey** .</span><span class="sxs-lookup"><span data-stu-id="3caca-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="3caca-146">Para depurar a parte do suplemento, definir pontos de interrupção apropriados no script que você adicionou.</span><span class="sxs-lookup"><span data-stu-id="3caca-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="3caca-147">Navegue até uma página PDP e escolha **Editar página** no menu Ferramentas (ícone de engrenagem).</span><span class="sxs-lookup"><span data-stu-id="3caca-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="3caca-148">Adicione a parte do **Título do GetProjectId** a uma web part na página.</span><span class="sxs-lookup"><span data-stu-id="3caca-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="3caca-149">A ID do projeto exibe **estendem** controle na página de web Parts.</span><span class="sxs-lookup"><span data-stu-id="3caca-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="3caca-150">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="3caca-150">Next steps</span></span>
<span data-ttu-id="3caca-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="3caca-151"></span></span>

<span data-ttu-id="3caca-152">A parte de suplemento neste exemplo não acessar dados do Project Server ou dados do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3caca-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="3caca-153">Você pode usar a identificação do produto para obter mais informações sobre o projeto atual usando um cliente API, como o modelo de objeto JavaScript ou o serviço REST.</span><span class="sxs-lookup"><span data-stu-id="3caca-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="3caca-154">No arquivo AppManifest.xml, especifique as permissões que seu suplemento precisa acessar dados do Project Server ou os dados do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3caca-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="3caca-155">Consulte [Criar Suplemento partes para instalar com o suplemento do SharePoint](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) para aprender a definir propriedades personalizadas de uma parte do suplemento.</span><span class="sxs-lookup"><span data-stu-id="3caca-155">See [Create add-in parts to install with your SharePoint Add-in](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="3caca-156">Exemplo: Obtendo a ID do projeto em uma parte add-in em uma página PDP</span><span class="sxs-lookup"><span data-stu-id="3caca-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="3caca-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="3caca-157"></span></span>

<span data-ttu-id="3caca-158">O exemplo a seguir é o código completo em página de GetProjectID.aspx do cliente da web part.</span><span class="sxs-lookup"><span data-stu-id="3caca-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="3caca-159">O código registra um ouvinte de eventos e um manipulador de eventos que recebe e analisa uma mensagem que contém a ID do projeto.</span><span class="sxs-lookup"><span data-stu-id="3caca-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="3caca-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="3caca-160">See also</span></span>

- [<span data-ttu-id="3caca-161">Tarefas de programação do Project</span><span class="sxs-lookup"><span data-stu-id="3caca-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="3caca-162">Criar um suplemento do Project Server hospedado pelo SharePoint</span><span class="sxs-lookup"><span data-stu-id="3caca-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="3caca-163">Criar partes de suplementos para instalação com o seu Suplemento do SharePoint</span><span class="sxs-lookup"><span data-stu-id="3caca-163">Create add-in parts to install with your SharePoint Add-in</span></span>](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

