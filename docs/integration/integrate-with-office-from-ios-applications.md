---
title: Integração do Office com aplicativos do iOS
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: O Office para iOS oferece uma solução extensível que permite a integração com aplicativos de terceiros. Este artigo descreve como você pode fazer a integração com o Office a partir do seu aplicativo iOS, passando usuários do seu aplicativo para o Office e, em seguida, retornando-os ao seu aplicativo.
ms.openlocfilehash: d17a096c17eadab0cd94ee1dce18e979e80fa65d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299741"
---
# <a name="integrate-with-office-from-ios-applications"></a><span data-ttu-id="69b77-104">Integração do Office com aplicativos do iOS</span><span class="sxs-lookup"><span data-stu-id="69b77-104">Integrate with Office from iOS applications</span></span>

<span data-ttu-id="69b77-105">O Office para iOS oferece uma solução extensível que permite a integração com aplicativos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="69b77-105">Office for iOS provides an extensible solution that enables integration with third-party applications.</span></span> <span data-ttu-id="69b77-106">Este artigo descreve como você pode fazer a integração com o Office a partir do seu aplicativo iOS, passando usuários do seu aplicativo para o Office e, em seguida, retornando-os ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69b77-106">This article describes how you can integrate with Office from your iOS application by passing users from your application to Office, and then returning them to your application.</span></span>
  
<span data-ttu-id="69b77-107">Você pode habilitar os usuários que estão executando o Office em um dispositivo iOS para abrir e editar arquivos armazenados no SharePoint ou no OneDrive de qualquer aplicativo e, em seguida, retorná-los rapidamente ao aplicativo original quando eles terminaram de editar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="69b77-107">You can enable users who are running Office on an iOS device to open and edit files stored in SharePoint or OneDrive from any application, and then quickly return them to the original application when they're done editing the file.</span></span> <span data-ttu-id="69b77-108">Para fazer isso, você passa arquivos para o Office por meio de identificadores de protocolo e garante que o Office será invocado de uma maneira que Office possa entender.</span><span class="sxs-lookup"><span data-stu-id="69b77-108">To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="69b77-109">Quando um usuário termina de editar um arquivo, ele pode escolher a seta para trás no aplicativo do Office para fechar o documento e retornar ao aplicativo de armazenamento original, desde que você passe informações específicas para o aplicativo do Office quando ele é iniciado.</span><span class="sxs-lookup"><span data-stu-id="69b77-109">When a user is done editing a file, they can choose the back arrow in the Office application to close the document and return to the original storage application, provided you pass specific information to the Office application when it launches.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="69b77-110">Verifique se o Office foi instalado</span><span class="sxs-lookup"><span data-stu-id="69b77-110">Verify that Office has been installed</span></span>

<span data-ttu-id="69b77-111">O aplicativo de referência primeiramente precisará verificar se um aplicativo específico do Office está instalado.</span><span class="sxs-lookup"><span data-stu-id="69b77-111">Your referring application will first need to verify that a particular Office application is installed.</span></span> <span data-ttu-id="69b77-112">Os seguintes aplicativos do Office podem ser instalados em dispositivos iOS para visualização e edição de documentos:</span><span class="sxs-lookup"><span data-stu-id="69b77-112">The following Office applications can be installed on iOS devices for document viewing and editing:</span></span>
  
- <span data-ttu-id="69b77-113">Excel</span><span class="sxs-lookup"><span data-stu-id="69b77-113">Excel</span></span>
    
- <span data-ttu-id="69b77-114">OneNote</span><span class="sxs-lookup"><span data-stu-id="69b77-114">OneNote</span></span>
    
- <span data-ttu-id="69b77-115">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="69b77-115">PowerPoint</span></span>
    
- <span data-ttu-id="69b77-116">Word</span><span class="sxs-lookup"><span data-stu-id="69b77-116">Word</span></span>
    
<span data-ttu-id="69b77-117">Use o método [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) para determinar se o aplicativo pode abrir o recurso.</span><span class="sxs-lookup"><span data-stu-id="69b77-117">Use the [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) method to determine whether your application can open the resource.</span></span> <span data-ttu-id="69b77-118">Este método obtém a URL do recurso como um parâmetro e retorna **não** se o aplicativo que aceita a URL não está disponível.</span><span class="sxs-lookup"><span data-stu-id="69b77-118">This method takes the URL for the resource as a parameter, and returns **No** if the application that accepts the URL is not available.</span></span> <span data-ttu-id="69b77-119">Se **CanOpenURL** **não**retornar, você precisará solicitar que o usuário instale o Office.</span><span class="sxs-lookup"><span data-stu-id="69b77-119">If **canOpenURL** returns **No**, you'll need to prompt the user to install Office.</span></span>
  
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="69b77-120">Solicitar que o usuário instale o Office</span><span class="sxs-lookup"><span data-stu-id="69b77-120">Prompt the user to install Office</span></span>

 <span data-ttu-id="69b77-121">Se um determinado aplicativo do Office não estiver instalado, você poderá usar um objeto [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) para renderizar a iTunes App Store em seu aplicativo e mostrar ao usuário o aplicativo do Office a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="69b77-121">If a particular Office application is not installed, you can use an [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) object to render the iTunes app store in your application and show the user the Office application to install.</span></span> <span data-ttu-id="69b77-122">A tabela a seguir lista o identificador iTunes a ser usado para invocar cada aplicativo do Office no controlador de exibição de produto do kit de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="69b77-122">The following table lists the iTunes identifier to use to invoke each Office application in the Store Kit Product View Controller.</span></span> 
  
|<span data-ttu-id="69b77-123">**Aplicativo do Office**</span><span class="sxs-lookup"><span data-stu-id="69b77-123">**Office application**</span></span>|<span data-ttu-id="69b77-124">**identificador iTunes**</span><span class="sxs-lookup"><span data-stu-id="69b77-124">**iTunes identifier**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69b77-125">Excel</span><span class="sxs-lookup"><span data-stu-id="69b77-125">Excel</span></span>  <br/> |[<span data-ttu-id="69b77-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp; UO = 4</span><span class="sxs-lookup"><span data-stu-id="69b77-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="69b77-127">OneNote (iPhone)</span><span class="sxs-lookup"><span data-stu-id="69b77-127">OneNote (iPhone)</span></span>  <br/> |[<span data-ttu-id="69b77-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp; UO = 4</span><span class="sxs-lookup"><span data-stu-id="69b77-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="69b77-129">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="69b77-129">PowerPoint</span></span>  <br/> |[<span data-ttu-id="69b77-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp; UO = 4</span><span class="sxs-lookup"><span data-stu-id="69b77-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="69b77-131">Word</span><span class="sxs-lookup"><span data-stu-id="69b77-131">Word</span></span>  <br/> |[<span data-ttu-id="69b77-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp; UO = 4</span><span class="sxs-lookup"><span data-stu-id="69b77-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="69b77-133">Usar o Office</span><span class="sxs-lookup"><span data-stu-id="69b77-133">Invoke Office</span></span>

<span data-ttu-id="69b77-134">Quando o aplicativo do Office estiver instalado, o aplicativo de referência poderá invocar Office passando os seguintes detalhes:</span><span class="sxs-lookup"><span data-stu-id="69b77-134">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span> 
  
- <span data-ttu-id="69b77-135">Protocolo do Office</span><span class="sxs-lookup"><span data-stu-id="69b77-135">Office protocol</span></span>
    
- <span data-ttu-id="69b77-136">Modo de abertura</span><span class="sxs-lookup"><span data-stu-id="69b77-136">Open mode</span></span>
    
- <span data-ttu-id="69b77-137">URL</span><span class="sxs-lookup"><span data-stu-id="69b77-137">URL</span></span>
    
- <span data-ttu-id="69b77-138">Protocolo passback</span><span class="sxs-lookup"><span data-stu-id="69b77-138">Passback protocol</span></span>
    
- <span data-ttu-id="69b77-139">Contexto do documento</span><span class="sxs-lookup"><span data-stu-id="69b77-139">Document context</span></span>
    
<span data-ttu-id="69b77-140">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="69b77-140">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
<span data-ttu-id="69b77-141">O exemplo a seguir mostra uma solicitação para invocar um arquivo do Word para edição:</span><span class="sxs-lookup"><span data-stu-id="69b77-141">The following example shows a request to invoke a Word file for editing:</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a><span data-ttu-id="69b77-142">Protocolos do Office</span><span class="sxs-lookup"><span data-stu-id="69b77-142">Office protocols</span></span>

<span data-ttu-id="69b77-143">A tabela a seguir lista os protocolos de cada aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="69b77-143">The following table lists the protocols for each Office application.</span></span> 
  
|<span data-ttu-id="69b77-144">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="69b77-144">**Application**</span></span>|<span data-ttu-id="69b77-145">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="69b77-145">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69b77-146">Excel</span><span class="sxs-lookup"><span data-stu-id="69b77-146">Excel</span></span>  <br/> |<span data-ttu-id="69b77-147">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="69b77-147">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="69b77-148">OneNote</span><span class="sxs-lookup"><span data-stu-id="69b77-148">OneNote</span></span>  <br/> |<span data-ttu-id="69b77-149">OneNote</span><span class="sxs-lookup"><span data-stu-id="69b77-149">onenote:</span></span>  <br/> |
|<span data-ttu-id="69b77-150">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="69b77-150">PowerPoint</span></span>  <br/> |<span data-ttu-id="69b77-151">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="69b77-151">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="69b77-152">Word</span><span class="sxs-lookup"><span data-stu-id="69b77-152">Word</span></span>  <br/> |<span data-ttu-id="69b77-153">ms-word:</span><span class="sxs-lookup"><span data-stu-id="69b77-153">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="69b77-154">Modo de abertura</span><span class="sxs-lookup"><span data-stu-id="69b77-154">Open mode</span></span>

<span data-ttu-id="69b77-155">Aplicativos do Office podem abrir arquivos diretamente no modo de exibição (ofv) ou editar o modo (ofe).</span><span class="sxs-lookup"><span data-stu-id="69b77-155">Office applications can open files directly into view (ofv) or edit (ofe) mode.</span></span> <span data-ttu-id="69b77-156">O modo de edição é o padrão.</span><span class="sxs-lookup"><span data-stu-id="69b77-156">Edit mode is the default.</span></span> 
  
<span data-ttu-id="69b77-157">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="69b77-157">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="69b77-158">URL</span><span class="sxs-lookup"><span data-stu-id="69b77-158">URL</span></span>

<span data-ttu-id="69b77-159">A URL inclui três partes:</span><span class="sxs-lookup"><span data-stu-id="69b77-159">The URL includes three parts:</span></span> 
  
- <span data-ttu-id="69b77-160">A declaração de que o arquivo será aberto para edição (ofe)</span><span class="sxs-lookup"><span data-stu-id="69b77-160">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="69b77-161">Descritor URL (| u |)</span><span class="sxs-lookup"><span data-stu-id="69b77-161">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="69b77-162">A URL</span><span class="sxs-lookup"><span data-stu-id="69b77-162">The URL</span></span>
    
<span data-ttu-id="69b77-163">A URL deve ser codificadt e deve ser um link direto para o arquivo (não um redirecionamento).</span><span class="sxs-lookup"><span data-stu-id="69b77-163">The URL has to be encoded and must be a direct link to the file (not a redirect).</span></span> <span data-ttu-id="69b77-164">Se a URL está em um formato que não dá suporte a Office ou o download falhar o Office não vai retornar o usuário aplicativo solicitado.</span><span class="sxs-lookup"><span data-stu-id="69b77-164">If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span> 
  
<span data-ttu-id="69b77-165">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="69b77-165">Schema format:</span></span>
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a><span data-ttu-id="69b77-166">Protocolo passback (opcional)</span><span class="sxs-lookup"><span data-stu-id="69b77-166">Passback protocol (optional)</span></span>

<span data-ttu-id="69b77-167">Se quiser que o Office retorne usuários para seu aplicativo iOS quando eles escolherem a seta para a direita, o aplicativo de invocação precisará usar o protocolo passback, que inclui o descritor ' | p | ' seguido do protocolo de aplicativo (sem dois-pontos).</span><span class="sxs-lookup"><span data-stu-id="69b77-167">If you want Office to return users to your iOS application when they choose the back arrow, the invoking application will need to use the passback protocol, which includes the descriptor '|p|' followed by the app protocol (without a colon).</span></span> <span data-ttu-id="69b77-168">Você precisará garantir que o aplicativo possa lidar corretamente com a resposta do Office.</span><span class="sxs-lookup"><span data-stu-id="69b77-168">You'll need to ensure that your application can properly handle the response from Office.</span></span>
  
<span data-ttu-id="69b77-169">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="69b77-169">Schema format:</span></span>
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a><span data-ttu-id="69b77-170">Contexto de documento (opcional)</span><span class="sxs-lookup"><span data-stu-id="69b77-170">Document context (optional)</span></span>

<span data-ttu-id="69b77-171">O Office não usa o contexto do documento, mas o aplicativo de referência pode precisar dele quando o Office passar um usuário de volta.</span><span class="sxs-lookup"><span data-stu-id="69b77-171">Office doesn't use the document context, but the referring application might need it when Office passes a user back.</span></span> <span data-ttu-id="69b77-172">Se quiser que o contexto do documento seja retornado para seu aplicativo, use o descritor ' | c | ' seguido do contexto desejado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="69b77-172">If you want the document context to be returned to your application, use the descriptor '|c|' followed by the context that you want as a string.</span></span> <span data-ttu-id="69b77-173">O Office não limita o tamanho da cadeia de caracteres, além de todos os limites impostos pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="69b77-173">Office does not limit the length of the string, beyond any limits imposed by the operating system.</span></span>
  
<span data-ttu-id="69b77-174">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="69b77-174">Schema format:</span></span>
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a><span data-ttu-id="69b77-175">Retornar usuários para o aplicativo de referência</span><span class="sxs-lookup"><span data-stu-id="69b77-175">Return users to the referring application</span></span>

<span data-ttu-id="69b77-176">Por motivos de segurança, o Office só retornará os usuários para o aplicativo de referência se o arquivo for aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="69b77-176">For security reasons, Office only returns users to the referring application if the file opened successfully.</span></span> <span data-ttu-id="69b77-177">Quando o usuário escolhe a seta para trás, o Office responde ao aplicativo que está chamando com o protocolo passback, o modo de abertura, a URL, o status de upload pendente e o contexto do documento.</span><span class="sxs-lookup"><span data-stu-id="69b77-177">When the user chooses the back arrow, Office responds to the invoking application with the passback protocol, open mode, URL, upload pending status, and document context.</span></span> <span data-ttu-id="69b77-178">O status de upload pendente usa o descritor | z | e é sim ou não.</span><span class="sxs-lookup"><span data-stu-id="69b77-178">The upload pending status uses the descriptor |z|, and is either yes or no.</span></span>
  
<span data-ttu-id="69b77-179">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="69b77-179">Schema format:</span></span>
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a><span data-ttu-id="69b77-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="69b77-180">See also</span></span>
<span data-ttu-id="69b77-181"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="69b77-181"></span></span>

- [<span data-ttu-id="69b77-182">método canOpenURL</span><span class="sxs-lookup"><span data-stu-id="69b77-182">canOpenURL method</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="69b77-183">Classe UIApplication</span><span class="sxs-lookup"><span data-stu-id="69b77-183">UIApplication class</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="69b77-184">Objeto SKProductViewController</span><span class="sxs-lookup"><span data-stu-id="69b77-184">SKProductViewController object</span></span>](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

