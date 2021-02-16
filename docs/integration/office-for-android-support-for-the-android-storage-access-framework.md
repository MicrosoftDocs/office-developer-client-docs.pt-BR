---
title: Suporte do Office para Android para a Estrutura de Acesso ao Armazenamento do Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: O Office para Android se integra à Estrutura de Acesso ao Armazenamento do Android, que permite ao Office abrir arquivos armazenados por outro provedor de documentos.
ms.openlocfilehash: 24d7e48106aeb5e58a668b94cbde00eaa9175230
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300347"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a><span data-ttu-id="c82ee-103">Suporte do Office para Android para a Estrutura de Acesso ao Armazenamento do Android</span><span class="sxs-lookup"><span data-stu-id="c82ee-103">Office for Android support for the Android Storage Access Framework</span></span>

<span data-ttu-id="c82ee-104">O Office para Android se integra à Estrutura de Acesso ao Armazenamento do Android, que permite ao Office abrir arquivos armazenados por outro provedor de documentos.</span><span class="sxs-lookup"><span data-stu-id="c82ee-104">Office for Android integrates with the Android Storage Access Framework, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="c82ee-105">O Android 4.4 (API nível 19) é o primeiro a incluir a Estrutura de Acesso ao Armazenamento (SAF).</span><span class="sxs-lookup"><span data-stu-id="c82ee-105">Android 4.4 (API level 19) introduces the Storage Access Framework (SAF).</span></span> <span data-ttu-id="c82ee-106">A SAF permite aos usuários navegar e abrir documentos, imagens e outros arquivos em todos os seus provedores de armazenamento de documento favoritos.</span><span class="sxs-lookup"><span data-stu-id="c82ee-106">The SAF enables users to browse and open documents, images, and other files across all their preferred document storage providers.</span></span> <span data-ttu-id="c82ee-107">Uma interface de usuário padrão permite aos usuários procurar arquivos e acessá-los de forma consistente entre aplicativos e provedores.</span><span class="sxs-lookup"><span data-stu-id="c82ee-107">A standard UI lets users browse files and access them in a consistent way across apps and providers.</span></span>
  
## <a name="implement-a-document-provider"></a><span data-ttu-id="c82ee-108">Implementar um provedor de documento</span><span class="sxs-lookup"><span data-stu-id="c82ee-108">Implement a document provider</span></span>

<span data-ttu-id="c82ee-109">Se você estiver desenvolvendo um aplicativo que fornece serviços de armazenamento para documentos, você pode disponibilizar arquivos por SAF [escrevendo um provedor de documentos personalizado](https://developer.android.com/guide/topics/providers/document-provider.html).</span><span class="sxs-lookup"><span data-stu-id="c82ee-109">If you're developing an app that provides storage services for documents, you can make your files available through the SAF by [writing a custom document provider](https://developer.android.com/guide/topics/providers/document-provider.html).</span></span> <span data-ttu-id="c82ee-110">Os aplicativos do Office poderão então usar a finalidade [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) e/ou [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) para receber os arquivos retornados ao seu provedor de documentos.</span><span class="sxs-lookup"><span data-stu-id="c82ee-110">Office apps can then invoke the [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) and/or [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) intent to receive the files returned by your document provider.</span></span> <span data-ttu-id="c82ee-111">Observe que a finalidade pode conter filtros para refinar ainda mais os critérios.</span><span class="sxs-lookup"><span data-stu-id="c82ee-111">Note that the intent might include filters to further refine the criteria.</span></span> 
  
## <a name="enable-free-consumer-edits"></a><span data-ttu-id="c82ee-112">Ativar edições de consumidor gratuito</span><span class="sxs-lookup"><span data-stu-id="c82ee-112">Enable free consumer edits</span></span>

<span data-ttu-id="c82ee-113">Os usuários podem entrar em aplicativos do Office com uma conta gratuita da Microsoft para criar ou editar documentos armazenados em um serviço de armazenamento direcionado ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="c82ee-113">Users can sign in to the Office apps with a free Microsoft account to create or edit docs that are stored in a consumer-oriented storage service.</span></span> <span data-ttu-id="c82ee-114">A tabela a seguir lista as propriedades obrigatórias que os provedores deverão fornecer como parte do cursor para habilitar a edição gratuita do consumidor para documentos acessados por meio da Estrutura de Acesso ao Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c82ee-114">The following table lists the mandatory properties that providers must supply as part of the cursor, to enable free consumer edit for documents accessed via the Storage Access Framework.</span></span>
  
|<span data-ttu-id="c82ee-115">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="c82ee-115">**Property**</span></span>|<span data-ttu-id="c82ee-116">**Índice**</span><span class="sxs-lookup"><span data-stu-id="c82ee-116">**Index**</span></span>|<span data-ttu-id="c82ee-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c82ee-117">**Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c82ee-118">Tipo de Documento</span><span class="sxs-lookup"><span data-stu-id="c82ee-118">Document Type</span></span>  <br/> |<span data-ttu-id="c82ee-119">com_microsoft_office_doctype</span><span class="sxs-lookup"><span data-stu-id="c82ee-119">com_microsoft_office_doctype</span></span>  <br/> |<span data-ttu-id="c82ee-120">\<consumidor\></span><span class="sxs-lookup"><span data-stu-id="c82ee-120">\<consumer\></span></span>  <br/> |
|<span data-ttu-id="c82ee-121">Nome amigável do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c82ee-121">Service Friendly Name</span></span>  <br/> |<span data-ttu-id="c82ee-122">com_microsoft_office_servicename</span><span class="sxs-lookup"><span data-stu-id="c82ee-122">com_microsoft_office_servicename</span></span>  <br/> |<span data-ttu-id="c82ee-123">Qualquer nome amigável para o serviço usado para identificar um documento na lista Recentes nos aplicativos do Office.</span><span class="sxs-lookup"><span data-stu-id="c82ee-123">Any user-friendly name for the service, used to identify a document in the Recent list in the Office apps.</span></span> <span data-ttu-id="c82ee-124">Observe que a propriedade "Contrato de termos de uso" deve ser fornecida antes do nome amigável para o serviço poder ser exibido.</span><span class="sxs-lookup"><span data-stu-id="c82ee-124">Note that the "Terms of Use Agreement" property must be supplied before the friendly name for the service can be displayed.</span></span>  <br/> |
|<span data-ttu-id="c82ee-125">Acordos de termos de uso</span><span class="sxs-lookup"><span data-stu-id="c82ee-125">Terms of Use Agreement</span></span>  <br/> |<span data-ttu-id="c82ee-126">com_microsoft_office_termsofuse</span><span class="sxs-lookup"><span data-stu-id="c82ee-126">com_microsoft_office_termsofuse</span></span>  <br/> |<span data-ttu-id="c82ee-127">\<Eu concordo com os termos localizados em https://go.microsoft.com/fwlink/p/?LinkId=528381\></span><span class="sxs-lookup"><span data-stu-id="c82ee-127">\<I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381\></span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c82ee-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c82ee-128">See also</span></span>
<span data-ttu-id="c82ee-129"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c82ee-129"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="c82ee-130">Integração com o Office</span><span class="sxs-lookup"><span data-stu-id="c82ee-130">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="c82ee-131">Noções básicas sobre provedores de conteúdo</span><span class="sxs-lookup"><span data-stu-id="c82ee-131">Content Provider Basics</span></span>](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [<span data-ttu-id="c82ee-132">Criar um provedor de conteúdo</span><span class="sxs-lookup"><span data-stu-id="c82ee-132">Creating a Content Provider</span></span>](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [<span data-ttu-id="c82ee-133">Guia para desenvolvedores da Estrutura de Acesso ao Armazenamento</span><span class="sxs-lookup"><span data-stu-id="c82ee-133">Storage Access Framework Developer Guide</span></span>](https://developer.android.com/guide/topics/providers/document-provider.html)
    

