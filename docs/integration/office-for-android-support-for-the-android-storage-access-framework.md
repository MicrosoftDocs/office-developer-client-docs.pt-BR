---
title: Suporte do Office para Android para a Estrutura de acesso ao armazenamento do Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office para Android integra-se a estrutura de acesso do armazenamento Android, que permite ao Office abrir arquivos armazenados pelo provedor de outro documento.
ms.openlocfilehash: c217eb2aa6c0974c32e60f5015449de7b157d39d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765763"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a><span data-ttu-id="356b1-103">Suporte do Office para Android para a Estrutura de acesso ao armazenamento do Android</span><span class="sxs-lookup"><span data-stu-id="356b1-103">Office for Android support for the Android Storage Access Framework</span></span>

<span data-ttu-id="356b1-104">Office para Android integra-se a estrutura de acesso do armazenamento Android, que permite ao Office abrir arquivos armazenados pelo provedor de outro documento.</span><span class="sxs-lookup"><span data-stu-id="356b1-104">Office for Android integrates with the Android Storage Access Framework, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="356b1-105">Android 4.4 (nível de API 19) apresenta a estrutura de acesso de armazenamento (SAF).</span><span class="sxs-lookup"><span data-stu-id="356b1-105">Android 4.4 (API level 19) introduces the Storage Access Framework (SAF).</span></span> <span data-ttu-id="356b1-106">O SAF permite que os usuários procurem e abrir documentos, imagens e outros arquivos entre todos os seus provedores de armazenamento de documento preferencial.</span><span class="sxs-lookup"><span data-stu-id="356b1-106">The SAF enables users to browse and open documents, images, and other files across all their preferred document storage providers.</span></span> <span data-ttu-id="356b1-107">Uma interface de usuário padrão permite aos usuários navegar por arquivos e acessá-las de forma consistente entre provedores e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="356b1-107">A standard UI lets users browse files and access them in a consistent way across apps and providers.</span></span>
  
## <a name="implement-a-document-provider"></a><span data-ttu-id="356b1-108">Implementar um provedor de documento</span><span class="sxs-lookup"><span data-stu-id="356b1-108">Implement a document provider</span></span>

<span data-ttu-id="356b1-109">Se você estiver desenvolvendo um aplicativo que fornece serviços de armazenamento de documentos, você pode fazer com que seus arquivos disponíveis por meio do SAF ao [escrever um provedor de documento personalizadas](https://developer.android.com/guide/topics/providers/document-provider.html).</span><span class="sxs-lookup"><span data-stu-id="356b1-109">If you're developing an app that provides storage services for documents, you can make your files available through the SAF by [writing a custom document provider](https://developer.android.com/guide/topics/providers/document-provider.html).</span></span> <span data-ttu-id="356b1-110">Aplicativos do Office podem então chamar a intenção [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) e/ou [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) para receber os arquivos retornados pelo seu provedor de documento.</span><span class="sxs-lookup"><span data-stu-id="356b1-110">Office apps can then invoke the [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) and/or [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) intent to receive the files returned by your document provider.</span></span> <span data-ttu-id="356b1-111">Observe que a intenção pode incluir filtros para refinar os critérios.</span><span class="sxs-lookup"><span data-stu-id="356b1-111">Note that the intent might include filters to further refine the criteria.</span></span> 
  
## <a name="enable-free-consumer-edits"></a><span data-ttu-id="356b1-112">Habilitar edições do consumidor gratuito</span><span class="sxs-lookup"><span data-stu-id="356b1-112">Enable free consumer edits</span></span>

<span data-ttu-id="356b1-113">Os usuários podem se conectar ao Office apps com uma conta da Microsoft gratuito para criar ou editar documentos armazenados em um serviço de armazenamento orientado ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="356b1-113">Users can sign in to the Office apps with a free Microsoft account to create or edit docs that are stored in a consumer-oriented storage service.</span></span> <span data-ttu-id="356b1-114">A tabela a seguir lista as propriedades obrigatórias que provedores deverá fornecer como parte do cursor, para ativar a edição de consumidor gratuito para documentos acessados por meio da estrutura de acesso de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="356b1-114">The following table lists the mandatory properties that providers must supply as part of the cursor, to enable free consumer edit for documents accessed via the Storage Access Framework.</span></span>
  
|<span data-ttu-id="356b1-115">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="356b1-115">**Property**</span></span>|<span data-ttu-id="356b1-116">**Index**</span><span class="sxs-lookup"><span data-stu-id="356b1-116">**Index**</span></span>|<span data-ttu-id="356b1-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="356b1-117">**Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="356b1-118">Tipo de documento</span><span class="sxs-lookup"><span data-stu-id="356b1-118">Document Type</span></span>  <br/> |<span data-ttu-id="356b1-119">com_microsoft_office_doctype</span><span class="sxs-lookup"><span data-stu-id="356b1-119">com_microsoft_office_doctype</span></span>  <br/> |<span data-ttu-id="356b1-120">\<consumidor\></span><span class="sxs-lookup"><span data-stu-id="356b1-120">\<consumer\></span></span>  <br/> |
|<span data-ttu-id="356b1-121">Nome amigável do serviço</span><span class="sxs-lookup"><span data-stu-id="356b1-121">Service Friendly Name</span></span>  <br/> |<span data-ttu-id="356b1-122">com_microsoft_office_servicename</span><span class="sxs-lookup"><span data-stu-id="356b1-122">com_microsoft_office_servicename</span></span>  <br/> |<span data-ttu-id="356b1-123">Qualquer nome amigável para o serviço, usado para identificar um documento na lista recente no Office apps.</span><span class="sxs-lookup"><span data-stu-id="356b1-123">Any user-friendly name for the service, used to identify a document in the Recent list in the Office apps.</span></span> <span data-ttu-id="356b1-124">Observe que a propriedade "Termos do contrato de uso" deve ser fornecida antes do nome amigável para o serviço pode ser exibido.</span><span class="sxs-lookup"><span data-stu-id="356b1-124">Note that the "Terms of Use Agreement" property must be supplied before the friendly name for the service can be displayed.</span></span>  <br/> |
|<span data-ttu-id="356b1-125">Termos do contrato de uso</span><span class="sxs-lookup"><span data-stu-id="356b1-125">Terms of Use Agreement</span></span>  <br/> |<span data-ttu-id="356b1-126">com_microsoft_office_termsofuse</span><span class="sxs-lookup"><span data-stu-id="356b1-126">com_microsoft_office_termsofuse</span></span>  <br/> |<span data-ttu-id="356b1-127">\<Eu concordar com os termos localizados emhttp://go.microsoft.com/fwlink/p/?LinkId=528381\></span><span class="sxs-lookup"><span data-stu-id="356b1-127">\<I agree to the terms located at http://go.microsoft.com/fwlink/p/?LinkId=528381\></span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="356b1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="356b1-128">See also</span></span>
<span data-ttu-id="356b1-129"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="356b1-129"></span></span>

- [<span data-ttu-id="356b1-130">Integração com o Office</span><span class="sxs-lookup"><span data-stu-id="356b1-130">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="356b1-131">Noções básicas do provedor de conteúdo</span><span class="sxs-lookup"><span data-stu-id="356b1-131">Content Provider Basics</span></span>](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [<span data-ttu-id="356b1-132">Criando um provedor de conteúdo</span><span class="sxs-lookup"><span data-stu-id="356b1-132">Creating a Content Provider</span></span>](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [<span data-ttu-id="356b1-133">Guia do desenvolvedor do armazenamento Access Framework</span><span class="sxs-lookup"><span data-stu-id="356b1-133">Storage Access Framework Developer Guide</span></span>](https://developer.android.com/guide/topics/providers/document-provider.html)
    

