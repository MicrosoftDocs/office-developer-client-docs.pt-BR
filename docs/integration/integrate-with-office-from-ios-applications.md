---
title: Integração do Office com aplicativos do iOS
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office para iOS fornece uma solução extensível que permite a integração com aplicativos de terceiros. Este artigo descreve como você pode integrar com o Office do seu aplicativo iOS passando os usuários de seu aplicativo para Office, e, em seguida, retornando-los ao seu aplicativo.
ms.openlocfilehash: 66106c51706a9ab1cd0e36b51340e65ccb807902
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595325"
---
# <a name="integrate-with-office-from-ios-applications"></a><span data-ttu-id="784b6-104">Integração do Office com aplicativos do iOS</span><span class="sxs-lookup"><span data-stu-id="784b6-104">Integrate with Office from iOS applications</span></span>

<span data-ttu-id="784b6-105">Office para iOS fornece uma solução extensível que permite a integração com aplicativos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="784b6-105">Office for iOS provides an extensible solution that enables integration with third-party applications.</span></span> <span data-ttu-id="784b6-106">Este artigo descreve como você pode integrar com o Office do seu aplicativo iOS passando os usuários de seu aplicativo para Office, e, em seguida, retornando-los ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="784b6-106">This article describes how you can integrate with Office from your iOS application by passing users from your application to Office, and then returning them to your application.</span></span>
  
<span data-ttu-id="784b6-107">Você pode permitir que os usuários que estão executando o Office em um dispositivo iOS para abrir e editar arquivos armazenados no SharePoint ou OneDrive de qualquer aplicativo e, em seguida, rapidamente voltar para o aplicativo original quando eles terminar edição do arquivo.</span><span class="sxs-lookup"><span data-stu-id="784b6-107">You can enable users who are running Office on an iOS device to open and edit files stored in SharePoint or OneDrive from any application, and then quickly return them to the original application when they're done editing the file.</span></span> <span data-ttu-id="784b6-108">Para fazer isso, você passa arquivos para o Office via manipuladores de protocolo e você se certificar de que o Office é invocado de forma que o Office pode entender.</span><span class="sxs-lookup"><span data-stu-id="784b6-108">To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="784b6-109">Quando um usuário é feito editando um arquivo, eles podem escolher na seta para voltar no aplicativo do Office para fechar o documento e retornar para o aplicativo de armazenamento original, desde que você passa informações específicas para o aplicativo do Office quando ele é iniciado.</span><span class="sxs-lookup"><span data-stu-id="784b6-109">When a user is done editing a file, they can choose the back arrow in the Office application to close the document and return to the original storage application, provided you pass specific information to the Office application when it launches.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="784b6-110">Verificar se o Office foi instalado</span><span class="sxs-lookup"><span data-stu-id="784b6-110">Verify that Office has been installed</span></span>

<span data-ttu-id="784b6-111">Seu aplicativo referência primeiro precisará verificar se um aplicativo específico do Office está instalado.</span><span class="sxs-lookup"><span data-stu-id="784b6-111">Your referring application will first need to verify that a particular Office application is installed.</span></span> <span data-ttu-id="784b6-112">Os seguintes aplicativos do Office podem ser instalados nos dispositivos de iOS para exibição e edição de documentos:</span><span class="sxs-lookup"><span data-stu-id="784b6-112">The following Office applications can be installed on iOS devices for document viewing and editing:</span></span>
  
- <span data-ttu-id="784b6-113">Excel</span><span class="sxs-lookup"><span data-stu-id="784b6-113">Excel</span></span>
    
- <span data-ttu-id="784b6-114">OneNote</span><span class="sxs-lookup"><span data-stu-id="784b6-114">OneNote</span></span>
    
- <span data-ttu-id="784b6-115">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="784b6-115">PowerPoint</span></span>
    
- <span data-ttu-id="784b6-116">Word</span><span class="sxs-lookup"><span data-stu-id="784b6-116">Word</span></span>
    
<span data-ttu-id="784b6-117">Use o método [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) para determinar se o seu aplicativo pode abrir o recurso.</span><span class="sxs-lookup"><span data-stu-id="784b6-117">Use the [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) method to determine whether your application can open the resource.</span></span> <span data-ttu-id="784b6-118">Esse método leva a URL para o recurso como um parâmetro e retorna **não** se o aplicativo que aceita a URL não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="784b6-118">This method takes the URL for the resource as a parameter, and returns **No** if the application that accepts the URL is not available.</span></span> <span data-ttu-id="784b6-119">Se **canOpenURL** retornará **não**, você precisará solicitar ao usuário para instalar o Office.</span><span class="sxs-lookup"><span data-stu-id="784b6-119">If **canOpenURL** returns **No**, you'll need to prompt the user to install Office.</span></span>
  
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="784b6-120">Solicita ao usuário para instalar o Office</span><span class="sxs-lookup"><span data-stu-id="784b6-120">Prompt the user to install Office</span></span>

 <span data-ttu-id="784b6-121">Se um aplicativo específico do Office não estiver instalado, você pode usar um objeto [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) para renderizar iTunes app store em seu aplicativo e mostrar ao usuário o aplicativo do Office para instalar.</span><span class="sxs-lookup"><span data-stu-id="784b6-121">If a particular Office application is not installed, you can use an [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) object to render the iTunes app store in your application and show the user the Office application to install.</span></span> <span data-ttu-id="784b6-122">A tabela a seguir lista o identificador do iTunes usar para invocar a cada aplicativo do Office no controlador de modo de exibição de produto do Kit de repositório.</span><span class="sxs-lookup"><span data-stu-id="784b6-122">The following table lists the iTunes identifier to use to invoke each Office application in the Store Kit Product View Controller.</span></span> 
  
|<span data-ttu-id="784b6-123">**Aplicativo do Office**</span><span class="sxs-lookup"><span data-stu-id="784b6-123">**Office application**</span></span>|<span data-ttu-id="784b6-124">**Identificador iTunes**</span><span class="sxs-lookup"><span data-stu-id="784b6-124">**iTunes identifier**</span></span>|
|:-----|:-----|
|<span data-ttu-id="784b6-125">Excel</span><span class="sxs-lookup"><span data-stu-id="784b6-125">Excel</span></span>  <br/> |[<span data-ttu-id="784b6-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp; uo = 4</span><span class="sxs-lookup"><span data-stu-id="784b6-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="784b6-127">OneNote (iPhone)</span><span class="sxs-lookup"><span data-stu-id="784b6-127">OneNote (iPhone)</span></span>  <br/> |[<span data-ttu-id="784b6-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp; uo = 4</span><span class="sxs-lookup"><span data-stu-id="784b6-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="784b6-129">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="784b6-129">PowerPoint</span></span>  <br/> |[<span data-ttu-id="784b6-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp; uo = 4</span><span class="sxs-lookup"><span data-stu-id="784b6-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="784b6-131">Word</span><span class="sxs-lookup"><span data-stu-id="784b6-131">Word</span></span>  <br/> |[<span data-ttu-id="784b6-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp; uo = 4</span><span class="sxs-lookup"><span data-stu-id="784b6-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="784b6-133">Invocar o Office</span><span class="sxs-lookup"><span data-stu-id="784b6-133">Invoke Office</span></span>

<span data-ttu-id="784b6-134">Quando o aplicativo do Office for instalado, o seu aplicativo referência pode chamar Office passando-se os seguintes detalhes:</span><span class="sxs-lookup"><span data-stu-id="784b6-134">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span> 
  
- <span data-ttu-id="784b6-135">Protocolo do Office</span><span class="sxs-lookup"><span data-stu-id="784b6-135">Office protocol</span></span>
    
- <span data-ttu-id="784b6-136">Modo de abertura</span><span class="sxs-lookup"><span data-stu-id="784b6-136">Open mode</span></span>
    
- <span data-ttu-id="784b6-137">URL</span><span class="sxs-lookup"><span data-stu-id="784b6-137">URL</span></span>
    
- <span data-ttu-id="784b6-138">Protocolo Passback</span><span class="sxs-lookup"><span data-stu-id="784b6-138">Passback protocol</span></span>
    
- <span data-ttu-id="784b6-139">Contexto de documento</span><span class="sxs-lookup"><span data-stu-id="784b6-139">Document context</span></span>
    
<span data-ttu-id="784b6-140">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="784b6-140">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
<span data-ttu-id="784b6-141">O exemplo a seguir mostra uma solicitação para chamar um arquivo do Word para edição:</span><span class="sxs-lookup"><span data-stu-id="784b6-141">The following example shows a request to invoke a Word file for editing:</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a><span data-ttu-id="784b6-142">Protocolos do Office</span><span class="sxs-lookup"><span data-stu-id="784b6-142">Office protocols</span></span>

<span data-ttu-id="784b6-143">A tabela a seguir lista os protocolos para cada aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="784b6-143">The following table lists the protocols for each Office application.</span></span> 
  
|<span data-ttu-id="784b6-144">**Application**</span><span class="sxs-lookup"><span data-stu-id="784b6-144">**Application**</span></span>|<span data-ttu-id="784b6-145">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="784b6-145">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="784b6-146">Excel</span><span class="sxs-lookup"><span data-stu-id="784b6-146">Excel</span></span>  <br/> |<span data-ttu-id="784b6-147">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="784b6-147">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="784b6-148">OneNote</span><span class="sxs-lookup"><span data-stu-id="784b6-148">OneNote</span></span>  <br/> |<span data-ttu-id="784b6-149">OneNote:</span><span class="sxs-lookup"><span data-stu-id="784b6-149">onenote:</span></span>  <br/> |
|<span data-ttu-id="784b6-150">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="784b6-150">PowerPoint</span></span>  <br/> |<span data-ttu-id="784b6-151">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="784b6-151">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="784b6-152">Word</span><span class="sxs-lookup"><span data-stu-id="784b6-152">Word</span></span>  <br/> |<span data-ttu-id="784b6-153">ms-word:</span><span class="sxs-lookup"><span data-stu-id="784b6-153">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="784b6-154">Modo de abertura</span><span class="sxs-lookup"><span data-stu-id="784b6-154">Open mode</span></span>

<span data-ttu-id="784b6-155">Aplicativos do Office podem abrir arquivos diretamente no modo de exibição (ofv) ou Editar modo (ofe).</span><span class="sxs-lookup"><span data-stu-id="784b6-155">Office applications can open files directly into view (ofv) or edit (ofe) mode.</span></span> <span data-ttu-id="784b6-156">Modo de edição é o padrão.</span><span class="sxs-lookup"><span data-stu-id="784b6-156">Edit mode is the default.</span></span> 
  
<span data-ttu-id="784b6-157">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="784b6-157">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="784b6-158">URL</span><span class="sxs-lookup"><span data-stu-id="784b6-158">URL</span></span>

<span data-ttu-id="784b6-159">A URL inclui três partes:</span><span class="sxs-lookup"><span data-stu-id="784b6-159">The URL includes three parts:</span></span> 
  
- <span data-ttu-id="784b6-160">A declaração de que o arquivo será aberto para edição (ofe)</span><span class="sxs-lookup"><span data-stu-id="784b6-160">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="784b6-161">O descritor de URL (| u |)</span><span class="sxs-lookup"><span data-stu-id="784b6-161">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="784b6-162">A URL</span><span class="sxs-lookup"><span data-stu-id="784b6-162">The URL</span></span>
    
<span data-ttu-id="784b6-163">A URL tem que ser codificada e deve ser um link direto para o arquivo (não um redirecionamento).</span><span class="sxs-lookup"><span data-stu-id="784b6-163">The URL has to be encoded and must be a direct link to the file (not a redirect).</span></span> <span data-ttu-id="784b6-164">Se a URL estiver em um formato Office não dá suporte ou o download simplesmente falhar, o Office não retornará o usuário ao aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="784b6-164">If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span> 
  
<span data-ttu-id="784b6-165">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="784b6-165">Schema format:</span></span>
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a><span data-ttu-id="784b6-166">Protocolo de Passback (opcional)</span><span class="sxs-lookup"><span data-stu-id="784b6-166">Passback protocol (optional)</span></span>

<span data-ttu-id="784b6-167">Se desejar que o Office para retornar usuários ao seu aplicativo iOS quando escolherem na seta para voltar, o aplicativo de invocação precisará usar o protocolo passback, que inclui o descritor ' | p |' seguido pelo protocolo app (sem dois-pontos).</span><span class="sxs-lookup"><span data-stu-id="784b6-167">If you want Office to return users to your iOS application when they choose the back arrow, the invoking application will need to use the passback protocol, which includes the descriptor '|p|' followed by the app protocol (without a colon).</span></span> <span data-ttu-id="784b6-168">Você precisará garantir que o seu aplicativo pode manipular corretamente a resposta do Office.</span><span class="sxs-lookup"><span data-stu-id="784b6-168">You'll need to ensure that your application can properly handle the response from Office.</span></span>
  
<span data-ttu-id="784b6-169">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="784b6-169">Schema format:</span></span>
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a><span data-ttu-id="784b6-170">Contexto de documento (opcional)</span><span class="sxs-lookup"><span data-stu-id="784b6-170">Document context (optional)</span></span>

<span data-ttu-id="784b6-171">Office não usa o contexto do documento, mas o aplicativo de referência talvez precisem quando Office passa de volta um usuário.</span><span class="sxs-lookup"><span data-stu-id="784b6-171">Office doesn't use the document context, but the referring application might need it when Office passes a user back.</span></span> <span data-ttu-id="784b6-172">Se desejar que o contexto do documento a ser retornado ao seu aplicativo, use o descritor ' | c |' seguido de contexto que deseja usar como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="784b6-172">If you want the document context to be returned to your application, use the descriptor '|c|' followed by the context that you want as a string.</span></span> <span data-ttu-id="784b6-173">Office não limitam o comprimento da cadeia de caracteres, além de quaisquer limites impostas pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="784b6-173">Office does not limit the length of the string, beyond any limits imposed by the operating system.</span></span>
  
<span data-ttu-id="784b6-174">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="784b6-174">Schema format:</span></span>
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a><span data-ttu-id="784b6-175">Retornar usuários para o aplicativo de referência</span><span class="sxs-lookup"><span data-stu-id="784b6-175">Return users to the referring application</span></span>

<span data-ttu-id="784b6-176">Por motivos de segurança, Office retorna apenas os usuários para o aplicativo de referência se o arquivo foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="784b6-176">For security reasons, Office only returns users to the referring application if the file opened successfully.</span></span> <span data-ttu-id="784b6-177">Quando o usuário escolhe regressivo seta para baixo, Office responde ao aplicativo de invocação com o protocolo passback, abra o carregamento de modo, URL, status pendente e contexto de documentos.</span><span class="sxs-lookup"><span data-stu-id="784b6-177">When the user chooses the back arrow, Office responds to the invoking application with the passback protocol, open mode, URL, upload pending status, and document context.</span></span> <span data-ttu-id="784b6-178">O carregamento de status pendente usa o descritor | z |, e é Sim ou não.</span><span class="sxs-lookup"><span data-stu-id="784b6-178">The upload pending status uses the descriptor |z|, and is either yes or no.</span></span>
  
<span data-ttu-id="784b6-179">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="784b6-179">Schema format:</span></span>
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a><span data-ttu-id="784b6-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="784b6-180">See also</span></span>
<span data-ttu-id="784b6-181"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="784b6-181"></span></span>

- [<span data-ttu-id="784b6-182">método canOpenURL</span><span class="sxs-lookup"><span data-stu-id="784b6-182">canOpenURL method</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="784b6-183">Classe de UIApplication</span><span class="sxs-lookup"><span data-stu-id="784b6-183">UIApplication class</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="784b6-184">Objeto SKProductViewController</span><span class="sxs-lookup"><span data-stu-id="784b6-184">SKProductViewController object</span></span>](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

