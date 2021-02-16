---
title: Integração com o Office em aplicativos do Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office para Android oferece uma solução extensiva que permite a integração com aplicativos de terceiros. É possível integrar com o Office a partir do seu aplicativo de Android passando usuários de seu aplicativo do Office.
ms.openlocfilehash: 4e674b3d66f3acba7e9c9c19e716ff0d73d803b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303147"
---
# <a name="integrate-with-office-from-android-applications"></a><span data-ttu-id="8073e-104">Integração com o Office em aplicativos do Android</span><span class="sxs-lookup"><span data-stu-id="8073e-104">Integrate with Office from Android applications</span></span>

<span data-ttu-id="8073e-105">Office para Android oferece uma solução extensiva que permite a integração com aplicativos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="8073e-105">Office for Android provides an extensible solution that enables integration with third-party applications.</span></span> <span data-ttu-id="8073e-106">É possível integrar com o Office a partir do seu aplicativo de Android passando usuários de seu aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="8073e-106">You can integrate with Office from your Android application by passing users from your application to Office.</span></span>
  
<span data-ttu-id="8073e-107">Você pode habilitar os usuários que estão executando o Office em um dispositivo Android para abrir e editar arquivos armazenados no SharePoint ou no OneDrive de qualquer aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8073e-107">You can enable users who are running Office on an Android device to open and edit files stored in SharePoint or OneDrive from any application.</span></span> <span data-ttu-id="8073e-108">Para fazer isso, você passa arquivos para o Office por meio de identificadores de protocolo e garante que o Office será invocado de uma maneira que Office possa entender.</span><span class="sxs-lookup"><span data-stu-id="8073e-108">To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="8073e-109">Quando um usuário concluir a edição de um arquivo, ele pode  escolher a tecla voltar no dispositivo para retornar ao aplicativo de armazenamento original.</span><span class="sxs-lookup"><span data-stu-id="8073e-109">When a user is done editing a file, they can choose the back key on the device to return to the original storage application.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="8073e-110">Verifique se o Office foi instalado</span><span class="sxs-lookup"><span data-stu-id="8073e-110">Verify that Office has been installed</span></span>

<span data-ttu-id="8073e-111">O aplicativo de referência primeiramente precisará verificar se um aplicativo específico do Office está instalado.</span><span class="sxs-lookup"><span data-stu-id="8073e-111">Your referring application will first need to verify that a particular Office application is installed.</span></span> <span data-ttu-id="8073e-112">Os seguintes aplicativos do Office podem ser instalados em dispositivos Android para documento visualização e edição:</span><span class="sxs-lookup"><span data-stu-id="8073e-112">The following Office applications can be installed on Android devices for document viewing and editing:</span></span> 
  
- <span data-ttu-id="8073e-113">Excel</span><span class="sxs-lookup"><span data-stu-id="8073e-113">Excel</span></span>
    
- <span data-ttu-id="8073e-114">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="8073e-114">PowerPoint</span></span>
    
- <span data-ttu-id="8073e-115">Word</span><span class="sxs-lookup"><span data-stu-id="8073e-115">Word</span></span>
    
<span data-ttu-id="8073e-116">Use o PackageManager Android para determinar se um aplicativo específico do Office está instalado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8073e-116">Use Android PackageManager to determine whether a particular Office application is installed on the device.</span></span> <span data-ttu-id="8073e-117">A tabela a seguir lista os nomes de pacote para os aplicativos do Office que você pode usar no processo.</span><span class="sxs-lookup"><span data-stu-id="8073e-117">The following table lists the package names for the Office applications that you can use in this process.</span></span>
  
|<span data-ttu-id="8073e-118">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="8073e-118">**Application**</span></span>|<span data-ttu-id="8073e-119">**Nome do pacote**</span><span class="sxs-lookup"><span data-stu-id="8073e-119">**Package name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8073e-120">Excel</span><span class="sxs-lookup"><span data-stu-id="8073e-120">Excel</span></span>  <br/> |<span data-ttu-id="8073e-121">com.microsoft.Office.Excel</span><span class="sxs-lookup"><span data-stu-id="8073e-121">com.microsoft.office.excel</span></span>  <br/> |
|<span data-ttu-id="8073e-122">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="8073e-122">PowerPoint</span></span>  <br/> |<span data-ttu-id="8073e-123">com.microsoft.Office.PowerPoint</span><span class="sxs-lookup"><span data-stu-id="8073e-123">com.microsoft.office.powerpoint</span></span>  <br/> |
|<span data-ttu-id="8073e-124">Word</span><span class="sxs-lookup"><span data-stu-id="8073e-124">Word</span></span>  <br/> |<span data-ttu-id="8073e-125">com.microsoft.Office.Word</span><span class="sxs-lookup"><span data-stu-id="8073e-125">com.microsoft.office.word</span></span>  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="8073e-126">Solicitar que o usuário instale o Office</span><span class="sxs-lookup"><span data-stu-id="8073e-126">Prompt the user to install Office</span></span>

<span data-ttu-id="8073e-127">Se um aplicativo específico do Office não estiver instalado, poderá solicitar ao usuário que instale o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8073e-127">If a particular Office application is not installed, you can prompt the user to install the application.</span></span> <span data-ttu-id="8073e-128">A tabela a seguir lista os locais disponíveis para instalação de aplicativos do Office.</span><span class="sxs-lookup"><span data-stu-id="8073e-128">The following table lists the available install locations for Office applications.</span></span>
  
|<span data-ttu-id="8073e-129">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="8073e-129">**Application**</span></span>|<span data-ttu-id="8073e-130">**Google Play Store**</span><span class="sxs-lookup"><span data-stu-id="8073e-130">**Google Play Store**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8073e-131">Excel</span><span class="sxs-lookup"><span data-stu-id="8073e-131">Excel</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|<span data-ttu-id="8073e-132">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="8073e-132">PowerPoint</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|<span data-ttu-id="8073e-133">Word</span><span class="sxs-lookup"><span data-stu-id="8073e-133">Word</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="8073e-134">Usar o Office</span><span class="sxs-lookup"><span data-stu-id="8073e-134">Invoke Office</span></span>

<span data-ttu-id="8073e-135">Quando o aplicativo do Office estiver instalado, o aplicativo de referência poderá invocar Office passando os seguintes detalhes:</span><span class="sxs-lookup"><span data-stu-id="8073e-135">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span>
  
- <span data-ttu-id="8073e-136">Protocolo do Office</span><span class="sxs-lookup"><span data-stu-id="8073e-136">Office protocol</span></span>
    
- <span data-ttu-id="8073e-137">Modo de abertura</span><span class="sxs-lookup"><span data-stu-id="8073e-137">Open mode</span></span>
    
- <span data-ttu-id="8073e-138">URL</span><span class="sxs-lookup"><span data-stu-id="8073e-138">URL</span></span>
    
<span data-ttu-id="8073e-139">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="8073e-139">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>`
  
<span data-ttu-id="8073e-140">O exemplo a seguir mostra uma solicitação para invocar um arquivo do Word para edição.</span><span class="sxs-lookup"><span data-stu-id="8073e-140">The following example shows a request to invoke a Word file for editing.</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a><span data-ttu-id="8073e-141">Protocolos do Office</span><span class="sxs-lookup"><span data-stu-id="8073e-141">Office protocols</span></span>

<span data-ttu-id="8073e-142">A tabela a seguir lista os protocolos de cada aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="8073e-142">The following table lists the protocols for each Office application.</span></span>
  
|<span data-ttu-id="8073e-143">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="8073e-143">**Application**</span></span>|<span data-ttu-id="8073e-144">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="8073e-144">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8073e-145">Excel</span><span class="sxs-lookup"><span data-stu-id="8073e-145">Excel</span></span>  <br/> |<span data-ttu-id="8073e-146">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="8073e-146">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="8073e-147">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="8073e-147">PowerPoint</span></span>  <br/> |<span data-ttu-id="8073e-148">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="8073e-148">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="8073e-149">Word</span><span class="sxs-lookup"><span data-stu-id="8073e-149">Word</span></span>  <br/> |<span data-ttu-id="8073e-150">ms-word:</span><span class="sxs-lookup"><span data-stu-id="8073e-150">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="8073e-151">Modo de abertura</span><span class="sxs-lookup"><span data-stu-id="8073e-151">Open mode</span></span>

<span data-ttu-id="8073e-152">Aplicativos do Office podem abrir arquivos diretamente no modo de exibição (ofv) ou editar o modo (ofe).</span><span class="sxs-lookup"><span data-stu-id="8073e-152">Office applications can open files directly into view (ofv) or edit (ofe) mode.</span></span> <span data-ttu-id="8073e-153">O modo de edição é o padrão.</span><span class="sxs-lookup"><span data-stu-id="8073e-153">Edit mode is the default.</span></span>
  
<span data-ttu-id="8073e-154">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="8073e-154">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="8073e-155">URL</span><span class="sxs-lookup"><span data-stu-id="8073e-155">URL</span></span>

<span data-ttu-id="8073e-156">A URL inclui três partes:</span><span class="sxs-lookup"><span data-stu-id="8073e-156">The URL includes three parts:</span></span>
  
- <span data-ttu-id="8073e-157">A declaração de que o arquivo será aberto para edição (ofe)</span><span class="sxs-lookup"><span data-stu-id="8073e-157">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="8073e-158">Descritor URL (| u |)</span><span class="sxs-lookup"><span data-stu-id="8073e-158">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="8073e-159">A URL</span><span class="sxs-lookup"><span data-stu-id="8073e-159">The URL</span></span>
    
<span data-ttu-id="8073e-160">A URL deve ser codificadt e deve ser um link direto para o arquivo (não um redirecionamento).</span><span class="sxs-lookup"><span data-stu-id="8073e-160">The URL has to be encoded and must be a direct link to the file (not a redirect).</span></span> <span data-ttu-id="8073e-161">Se a URL está em um formato que não dá suporte a Office ou o download falhar o Office não vai retornar o usuário aplicativo solicitado.</span><span class="sxs-lookup"><span data-stu-id="8073e-161">If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span>
  
<span data-ttu-id="8073e-162">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="8073e-162">Schema format:</span></span>
  
 `|u|<document URL>`
  
## <a name="see-also"></a><span data-ttu-id="8073e-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="8073e-163">See also</span></span>
<span data-ttu-id="8073e-164"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="8073e-164"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="8073e-165">Integração com o Office</span><span class="sxs-lookup"><span data-stu-id="8073e-165">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="8073e-166">PackageManager</span><span class="sxs-lookup"><span data-stu-id="8073e-166">PackageManager</span></span>](https://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [<span data-ttu-id="8073e-167">GetPackageManager()</span><span class="sxs-lookup"><span data-stu-id="8073e-167">GetPackageManager()</span></span>](https://developer.android.com/reference/android/content/Context.html)
    

