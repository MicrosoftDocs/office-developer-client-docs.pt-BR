---
title: Propriedade canônica PidTagExchangeProfileSectionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699510"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="d4eb5-103">Propriedade canônica PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="d4eb5-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="d4eb5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4eb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4eb5-105">Contém um GUID gerado dinamicamente usado para determinar uma conta quando você estiver usando várias contas do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4eb5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d4eb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4eb5-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="d4eb5-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="d4eb5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d4eb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4eb5-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="d4eb5-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="d4eb5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d4eb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4eb5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d4eb5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d4eb5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d4eb5-112">Area:</span></span>  <br/> |<span data-ttu-id="d4eb5-113">Várias contas do Exchange</span><span class="sxs-lookup"><span data-stu-id="d4eb5-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4eb5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4eb5-114">Remarks</span></span>

<span data-ttu-id="d4eb5-115">Microsoft Outlook 2010 e o Microsoft Outlook 2013 suportam várias contas do Exchange, em vez de uma única conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="d4eb5-116">Para acomodar várias contas do Exchange, o layout do perfil MAPI foi alterado.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="d4eb5-117">No Microsoft Office Outlook 2007 e versões anteriores, perfis contidos uma seção de perfil fixa dedicada para configurações do Exchange, como o nome do servidor, nome de usuário e o arquivo de pasta Offline (. ost).</span><span class="sxs-lookup"><span data-stu-id="d4eb5-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="d4eb5-118">local.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-118">location.</span></span> <span data-ttu-id="d4eb5-119">Essas configurações foram identificadas usando um identificador exclusivo, a propriedade **pbGlobalProfileSectionGuid** .</span><span class="sxs-lookup"><span data-stu-id="d4eb5-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="d4eb5-120">A seção usada para configurações do Exchange é chamada a seção de perfil Global do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="d4eb5-121">Um local de seção perfil fixo não mais é suficiente para acomodar várias contas do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="d4eb5-122">Em vez disso, para cada conta do Exchange no seu perfil, existe uma seção dedicada ao configurações dessa conta.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="d4eb5-123">Nova seção usada para configurações do Exchange é identificada pelo identificador exclusivo **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="d4eb5-124">A seção de perfil de serviço de mensagem para a conta do Exchange, você encontrará uma propriedade que contenha um GUID que seja gerado dinamicamente no momento em que a conta é criada.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="d4eb5-125">Este GUID é armazenado na propriedade **PidTagExchangeProfileSectionId** .</span><span class="sxs-lookup"><span data-stu-id="d4eb5-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="d4eb5-126">Repositórios de mensagem e contêineres do catálogo de endereços expõem uma propriedade para determinar qual eles pertencem a conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="d4eb5-127">Acessível na tabela de serviços de mensagem, cada serviço Exchange expõe essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="d4eb5-128">É possível recuperar essa propriedade por meio de uma chamada para [IMAPIProp::GetProps](imapiprop-getprops.md) em **PidTagExchangeProfileSectionId** após consultando para qualquer uma das seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="d4eb5-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="d4eb5-129">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d4eb5-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="d4eb5-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d4eb5-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="d4eb5-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d4eb5-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="d4eb5-132">Se o objeto não é associado com o Exchange, a chamada retorna **E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="d4eb5-133">Você pode restringir contêineres em um **PidTagExchangeProfileSectionId** ao exibir o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="d4eb5-134">Depois que você tiver um contêiner aberto, você pode consultar **emsmdbUID** a partir dele.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="d4eb5-135">Também é importante observar que se um destinatário foi selecionado de um catálogo de endereços do Exchange, o destinatário também tiver a **PidTagExchangeProfileSectionId** em sua lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d4eb5-136">Em toda as amostras de código e cabeçalhos de função, este GUID é conhecido como **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="d4eb5-137">Uma das contas Exchange está marcada como conta legada do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="d4eb5-138">Geralmente, é a primeira conta adicionada ao perfil.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="d4eb5-139">Todas as chamadas para abrir **pbGlobalProfileSectionGuid** é redirecionada para a seção global do Exchange da conta de legado.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="d4eb5-140">As chamadas de modelo de objeto que interagem com a conta do Exchange não-herdada também interagem com a conta legada do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="d4eb5-141">O serviço Exchange herdado tem a propriedade **PR_EMSMDB_LEGACY** (0x3D18000B), que é definido como **true** na tabela de serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="d4eb5-142">O herdado **emsmdbUID** também é marcada na Global seção perfil do Outlook do perfil como **PidTagExchangeProfileSectionId**.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="d4eb5-143">Código escrito para dar suporte a várias contas do Exchange não deve ter que recuperar o herdado **emsmdbUID** porque ele deve obter o correto **emsmdbUID**, dependendo da conta em com que seu código está interagindo.</span><span class="sxs-lookup"><span data-stu-id="d4eb5-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d4eb5-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4eb5-144">See also</span></span>



[<span data-ttu-id="d4eb5-145">Usar várias contas do Exchange</span><span class="sxs-lookup"><span data-stu-id="d4eb5-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="d4eb5-146">Como abrir a seção perfil Global</span><span class="sxs-lookup"><span data-stu-id="d4eb5-146">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

