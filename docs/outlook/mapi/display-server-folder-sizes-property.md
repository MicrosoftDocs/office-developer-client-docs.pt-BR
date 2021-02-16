---
title: Exibir a propriedade Tamanhos de Pasta do Servidor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434547"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="7addb-103">Exibir a propriedade Tamanhos de Pasta do Servidor</span><span class="sxs-lookup"><span data-stu-id="7addb-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="7addb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7addb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7addb-105">Exibe os tamanhos das pastas especificadas no servidor na caixa de diálogo Tamanho da Pasta **do** Outlook.</span><span class="sxs-lookup"><span data-stu-id="7addb-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7addb-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="7addb-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7addb-107">Exposto em:</span><span class="sxs-lookup"><span data-stu-id="7addb-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="7addb-108">[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="7addb-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="7addb-109">Criado por:</span><span class="sxs-lookup"><span data-stu-id="7addb-109">Created by:</span></span>  <br/> |<span data-ttu-id="7addb-110">Provedor da Loja</span><span class="sxs-lookup"><span data-stu-id="7addb-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="7addb-111">Acessado por:</span><span class="sxs-lookup"><span data-stu-id="7addb-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="7addb-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="7addb-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="7addb-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="7addb-113">Property type:</span></span>  <br/> |<span data-ttu-id="7addb-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7addb-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7addb-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="7addb-115">Access type:</span></span>  <br/> |<span data-ttu-id="7addb-116">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7addb-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7addb-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7addb-117">Remarks</span></span>

<span data-ttu-id="7addb-118">Para fornecer qualquer uma das funcionalidades do armazenamento, o provedor de armazenamento deve implementar [IMAPIProp : IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="7addb-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="7addb-119">Quando a marca de propriedade de qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor de propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="7addb-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="7addb-120">Os provedores da loja podem [chamar HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7addb-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="7addb-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="7addb-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="7addb-122">Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a [estrutura MAPINAMEID](mapinameid.md) apontada pelo parâmetro de entrada  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="7addb-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7addb-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="7addb-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="7addb-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="7addb-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="7addb-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="7addb-125">ulKind:</span></span>  <br/> |<span data-ttu-id="7addb-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="7addb-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="7addb-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="7addb-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="7addb-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span><span class="sxs-lookup"><span data-stu-id="7addb-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="7addb-129">Essa propriedade é suportada no Microsoft Outlook 2003 Service Pack (SP) 1.</span><span class="sxs-lookup"><span data-stu-id="7addb-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="7addb-130">Se a versão do Outlook for anterior ao Outlook 2003 SP 1 ou se seu valor for **falso,** o Outlook exibirá apenas os tamanhos de pastas no armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="7addb-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="7addb-131">Se essa propriedade for definida em um armazenamento que usa o Outlook 2003 SP 1, o Outlook consultará o tamanho de cada pasta especificada no servidor e na unidade local.</span><span class="sxs-lookup"><span data-stu-id="7addb-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="7addb-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then itries for **PR_MESSAGE_SIZE_EXTENDED**.</span><span class="sxs-lookup"><span data-stu-id="7addb-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="7addb-133">Em seguida, o provedor de armazenamento deve retornar o tamanho da pasta no servidor.</span><span class="sxs-lookup"><span data-stu-id="7addb-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="7addb-134">Para consultar o tamanho de uma pasta na unidade local, o Outlook abre a pasta sem o **sinalizador MAPI_NO_CACHE** local.</span><span class="sxs-lookup"><span data-stu-id="7addb-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="7addb-135">Em seguida, ele **consulta** PR_MESSAGE_SIZE_EXTENDED ; o provedor de armazenamento deve retornar o tamanho da pasta especificada na unidade local.</span><span class="sxs-lookup"><span data-stu-id="7addb-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="7addb-136">Com esse conjunto de propriedades, os provedores de armazenamento que sincronizam o conteúdo do armazenamento com um servidor podem exibir dados de tamanho de pasta no servidor na caixa de diálogo Tamanho da Pasta **do** Outlook.</span><span class="sxs-lookup"><span data-stu-id="7addb-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="7addb-137">Os usuários podem então comparar o uso atual do armazenamento do servidor com as cotas do servidor.</span><span class="sxs-lookup"><span data-stu-id="7addb-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

