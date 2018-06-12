---
title: Integração com o Office de aplicativos do Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office para Android fornece uma solução extensível que permite a integração com aplicativos de terceiros. É possível integrar com o Office a partir de seu aplicativo Android passando-se os usuários de seu aplicativo para o Office.
ms.openlocfilehash: 2fd60c7e86d3390bc5343f3e09fb2235f97e0b13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765722"
---
# <a name="integrate-with-office-from-android-applications"></a><span data-ttu-id="950be-104">Integração com o Office de aplicativos do Android</span><span class="sxs-lookup"><span data-stu-id="950be-104">Integrate with Office from Android applications</span></span>

<span data-ttu-id="950be-105">Office para Android fornece uma solução extensível que permite a integração com aplicativos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="950be-105">Office for Android provides an extensible solution that enables integration with third-party applications.</span></span> <span data-ttu-id="950be-106">É possível integrar com o Office a partir de seu aplicativo Android passando-se os usuários de seu aplicativo para o Office.</span><span class="sxs-lookup"><span data-stu-id="950be-106">You can integrate with Office from your Android application by passing users from your application to Office.</span></span>
  
<span data-ttu-id="950be-107">Você pode permitir que os usuários que estiverem executando o Office em um dispositivo Android para abrir e editar arquivos armazenados no SharePoint ou OneDrive de qualquer aplicativo.</span><span class="sxs-lookup"><span data-stu-id="950be-107">You can enable users who are running Office on an Android device to open and edit files stored in SharePoint or OneDrive from any application.</span></span> <span data-ttu-id="950be-108">Para fazer isso, você passa arquivos para o Office via manipuladores de protocolo e você se certificar de que o Office é invocado de forma que o Office pode entender.</span><span class="sxs-lookup"><span data-stu-id="950be-108">To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="950be-109">Quando um usuário é feito editando um arquivo, eles podem escolher a chave voltar no dispositivo para voltar para o aplicativo de armazenamento original.</span><span class="sxs-lookup"><span data-stu-id="950be-109">When a user is done editing a file, they can choose the back key on the device to return to the original storage application.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="950be-110">Verificar se o Office foi instalado</span><span class="sxs-lookup"><span data-stu-id="950be-110">Verify that Office has been installed</span></span>

<span data-ttu-id="950be-111">Seu aplicativo referência primeiro precisará verificar se um aplicativo específico do Office está instalado.</span><span class="sxs-lookup"><span data-stu-id="950be-111">Your referring application will first need to verify that a particular Office application is installed.</span></span> <span data-ttu-id="950be-112">Os seguintes aplicativos do Office podem ser instalados em dispositivos Android para exibição e edição de documentos:</span><span class="sxs-lookup"><span data-stu-id="950be-112">The following Office applications can be installed on Android devices for document viewing and editing:</span></span> 
  
- <span data-ttu-id="950be-113">Excel</span><span class="sxs-lookup"><span data-stu-id="950be-113">Excel</span></span>
    
- <span data-ttu-id="950be-114">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="950be-114">PowerPoint</span></span>
    
- <span data-ttu-id="950be-115">Word</span><span class="sxs-lookup"><span data-stu-id="950be-115">Word</span></span>
    
<span data-ttu-id="950be-116">Use o Android PackageManager para determinar se um aplicativo específico do Office está instalado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="950be-116">Use Android PackageManager to determine whether a particular Office application is installed on the device.</span></span> <span data-ttu-id="950be-117">A tabela a seguir lista os nomes de pacote para os aplicativos do Office que você pode usar nesse processo.</span><span class="sxs-lookup"><span data-stu-id="950be-117">The following table lists the package names for the Office applications that you can use in this process.</span></span>
  
|<span data-ttu-id="950be-118">**Application**</span><span class="sxs-lookup"><span data-stu-id="950be-118">**Application**</span></span>|<span data-ttu-id="950be-119">**Nome do pacote**</span><span class="sxs-lookup"><span data-stu-id="950be-119">**Package name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="950be-120">Excel</span><span class="sxs-lookup"><span data-stu-id="950be-120">Excel</span></span>  <br/> |<span data-ttu-id="950be-121">com.microsoft.Office.Excel</span><span class="sxs-lookup"><span data-stu-id="950be-121">com.microsoft.office.excel</span></span>  <br/> |
|<span data-ttu-id="950be-122">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="950be-122">PowerPoint</span></span>  <br/> |<span data-ttu-id="950be-123">com.microsoft.Office.PowerPoint</span><span class="sxs-lookup"><span data-stu-id="950be-123">com.microsoft.office.powerpoint</span></span>  <br/> |
|<span data-ttu-id="950be-124">Word</span><span class="sxs-lookup"><span data-stu-id="950be-124">Word</span></span>  <br/> |<span data-ttu-id="950be-125">com.microsoft.Office.Word</span><span class="sxs-lookup"><span data-stu-id="950be-125">com.microsoft.office.word</span></span>  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="950be-126">Solicita ao usuário para instalar o Office</span><span class="sxs-lookup"><span data-stu-id="950be-126">Prompt the user to install Office</span></span>

<span data-ttu-id="950be-127">Se um aplicativo específico do Office não estiver instalado, você pode solicitar o usuário para instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="950be-127">If a particular Office application is not installed, you can prompt the user to install the application.</span></span> <span data-ttu-id="950be-128">A tabela a seguir lista os locais de instalação disponíveis para aplicativos do Office.</span><span class="sxs-lookup"><span data-stu-id="950be-128">The following table lists the available install locations for Office applications.</span></span>
  
|<span data-ttu-id="950be-129">**Application**</span><span class="sxs-lookup"><span data-stu-id="950be-129">**Application**</span></span>|<span data-ttu-id="950be-130">**Repositório de tocar do Google**</span><span class="sxs-lookup"><span data-stu-id="950be-130">**Google Play Store**</span></span>|
|:-----|:-----|
|<span data-ttu-id="950be-131">Excel</span><span class="sxs-lookup"><span data-stu-id="950be-131">Excel</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|<span data-ttu-id="950be-132">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="950be-132">PowerPoint</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|<span data-ttu-id="950be-133">Word</span><span class="sxs-lookup"><span data-stu-id="950be-133">Word</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="950be-134">Invocar o Office</span><span class="sxs-lookup"><span data-stu-id="950be-134">Invoke Office</span></span>

<span data-ttu-id="950be-135">Quando o aplicativo do Office for instalado, o seu aplicativo referência pode chamar Office passando-se os seguintes detalhes:</span><span class="sxs-lookup"><span data-stu-id="950be-135">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span>
  
- <span data-ttu-id="950be-136">Protocolo do Office</span><span class="sxs-lookup"><span data-stu-id="950be-136">Office protocol</span></span>
    
- <span data-ttu-id="950be-137">Modo de abertura</span><span class="sxs-lookup"><span data-stu-id="950be-137">Open mode</span></span>
    
- <span data-ttu-id="950be-138">URL</span><span class="sxs-lookup"><span data-stu-id="950be-138">URL</span></span>
    
<span data-ttu-id="950be-139">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="950be-139">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>`
  
<span data-ttu-id="950be-140">O exemplo a seguir mostra uma solicitação para chamar um arquivo do Word para edição.</span><span class="sxs-lookup"><span data-stu-id="950be-140">The following example shows a request to invoke a Word file for editing.</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a><span data-ttu-id="950be-141">Protocolos do Office</span><span class="sxs-lookup"><span data-stu-id="950be-141">Office protocols</span></span>

<span data-ttu-id="950be-142">A tabela a seguir lista os protocolos para cada aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="950be-142">The following table lists the protocols for each Office application.</span></span>
  
|<span data-ttu-id="950be-143">**Application**</span><span class="sxs-lookup"><span data-stu-id="950be-143">**Application**</span></span>|<span data-ttu-id="950be-144">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="950be-144">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="950be-145">Excel</span><span class="sxs-lookup"><span data-stu-id="950be-145">Excel</span></span>  <br/> |<span data-ttu-id="950be-146">MS excel:</span><span class="sxs-lookup"><span data-stu-id="950be-146">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="950be-147">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="950be-147">PowerPoint</span></span>  <br/> |<span data-ttu-id="950be-148">MS-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="950be-148">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="950be-149">Word</span><span class="sxs-lookup"><span data-stu-id="950be-149">Word</span></span>  <br/> |<span data-ttu-id="950be-150">MS-word:</span><span class="sxs-lookup"><span data-stu-id="950be-150">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="950be-151">Modo de abertura</span><span class="sxs-lookup"><span data-stu-id="950be-151">Open mode</span></span>

<span data-ttu-id="950be-152">Aplicativos do Office podem abrir arquivos diretamente no modo de exibição (ofv) ou Editar modo (ofe).</span><span class="sxs-lookup"><span data-stu-id="950be-152">Office applications can open files directly into view (ofv) or edit (ofe) mode.</span></span> <span data-ttu-id="950be-153">Modo de edição é o padrão.</span><span class="sxs-lookup"><span data-stu-id="950be-153">Edit mode is the default.</span></span>
  
<span data-ttu-id="950be-154">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="950be-154">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="950be-155">URL</span><span class="sxs-lookup"><span data-stu-id="950be-155">URL</span></span>

<span data-ttu-id="950be-156">A URL inclui três partes:</span><span class="sxs-lookup"><span data-stu-id="950be-156">The URL includes three parts:</span></span>
  
- <span data-ttu-id="950be-157">A declaração de que o arquivo será aberto para edição (ofe)</span><span class="sxs-lookup"><span data-stu-id="950be-157">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="950be-158">O descritor de URL (| u |)</span><span class="sxs-lookup"><span data-stu-id="950be-158">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="950be-159">A URL</span><span class="sxs-lookup"><span data-stu-id="950be-159">The URL</span></span>
    
<span data-ttu-id="950be-160">A URL tem que ser codificada e deve ser um link direto para o arquivo (não um redirecionamento).</span><span class="sxs-lookup"><span data-stu-id="950be-160">The URL has to be encoded and must be a direct link to the file (not a redirect).</span></span> <span data-ttu-id="950be-161">Se a URL estiver em um formato Office não dá suporte ou o download simplesmente falhar, o Office não retornará o usuário ao aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="950be-161">If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span>
  
<span data-ttu-id="950be-162">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="950be-162">Schema format:</span></span>
  
 `|u|<document URL>`
  
## <a name="see-also"></a><span data-ttu-id="950be-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="950be-163">See also</span></span>
<span data-ttu-id="950be-164"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="950be-164"></span></span>

- [<span data-ttu-id="950be-165">Integração com o Office</span><span class="sxs-lookup"><span data-stu-id="950be-165">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="950be-166">PackageManager</span><span class="sxs-lookup"><span data-stu-id="950be-166">PackageManager</span></span>](http://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [<span data-ttu-id="950be-167">GetPackageManager()</span><span class="sxs-lookup"><span data-stu-id="950be-167">GetPackageManager()</span></span>](http://developer.android.com/reference/android/content/Context.html)
    

