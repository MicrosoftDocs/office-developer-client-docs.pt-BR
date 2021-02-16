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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316426"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="f48d7-103">Propriedade canônica PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="f48d7-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="f48d7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f48d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f48d7-105">Contém um GUID gerado dinamicamente usado para determinar uma conta quando você estiver usando várias contas do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f48d7-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f48d7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f48d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f48d7-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="f48d7-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="f48d7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f48d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f48d7-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="f48d7-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="f48d7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f48d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="f48d7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f48d7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f48d7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f48d7-112">Area:</span></span>  <br/> |<span data-ttu-id="f48d7-113">Várias contas do Exchange</span><span class="sxs-lookup"><span data-stu-id="f48d7-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f48d7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f48d7-114">Remarks</span></span>

<span data-ttu-id="f48d7-115">O Microsoft Outlook 2010 e o Microsoft Outlook 2013 suportam várias contas do Exchange em vez de uma única conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="f48d7-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="f48d7-116">Para acomodar várias contas do Exchange, o layout de perfil MAPI foi alterado.</span><span class="sxs-lookup"><span data-stu-id="f48d7-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="f48d7-117">No Microsoft Office Outlook 2007 e versões anteriores, os perfis continham uma seção de perfil fixa dedicada às configurações do Exchange, como nome do servidor, nome de usuário e arquivo de Pasta Offline (.ost).</span><span class="sxs-lookup"><span data-stu-id="f48d7-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="f48d7-118">local.</span><span class="sxs-lookup"><span data-stu-id="f48d7-118">location.</span></span> <span data-ttu-id="f48d7-119">Essas configurações foram identificadas usando um identificador exclusivo, a **propriedade pbGlobalProfileSectionGuid.**</span><span class="sxs-lookup"><span data-stu-id="f48d7-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="f48d7-120">A seção usada para as configurações do Exchange é chamada de Seção de Perfil Global do Exchange.</span><span class="sxs-lookup"><span data-stu-id="f48d7-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="f48d7-121">Um local de seção de perfil fixo não é mais suficiente para acomodar várias contas do Exchange.</span><span class="sxs-lookup"><span data-stu-id="f48d7-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="f48d7-122">Em vez disso, para cada conta do Exchange em seu perfil, existe uma seção dedicada às configurações dessa conta.</span><span class="sxs-lookup"><span data-stu-id="f48d7-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="f48d7-123">A nova seção usada para as configurações do Exchange é identificada pelo identificador exclusivo **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="f48d7-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="f48d7-124">Na seção de perfil de serviço de mensagens para a conta do Exchange, você pode encontrar uma propriedade que contém um GUID que é gerado dinamicamente no momento em que a conta é criada.</span><span class="sxs-lookup"><span data-stu-id="f48d7-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="f48d7-125">Esse GUID é armazenado na propriedade **PidTagExchangeProfileSectionId.**</span><span class="sxs-lookup"><span data-stu-id="f48d7-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="f48d7-126">Os armazenamentos de mensagens e os contêineres do livro de endereços expõem uma propriedade para determinar a qual conta do Exchange pertencem.</span><span class="sxs-lookup"><span data-stu-id="f48d7-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="f48d7-127">Acessível na tabela de serviços de mensagens, cada serviço do Exchange expõe essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f48d7-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="f48d7-128">Você pode recuperar essa propriedade por meio de uma chamada para [IMAPIProp::GetProps](imapiprop-getprops.md) em **PidTagExchangeProfileSectionId** após consultar qualquer uma das seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="f48d7-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="f48d7-129">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f48d7-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="f48d7-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f48d7-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="f48d7-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f48d7-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="f48d7-132">Se o objeto não estiver associado ao Exchange, a chamada retornará **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="f48d7-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="f48d7-133">Você pode restringir contêineres em **um PidTagExchangeProfileSectionId** ao exibir o livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="f48d7-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="f48d7-134">Depois de abrir um contêiner, você poderá consultar **o emsmdbUID** a partir dele.</span><span class="sxs-lookup"><span data-stu-id="f48d7-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="f48d7-135">Também vale a pena notar que, se um destinatário foi selecionado de um livro de endereços do Exchange, o destinatário também tem o **PidTagExchangeProfileSectionId** em sua lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f48d7-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f48d7-136">Em todos os exemplos de código e de função, esse GUID é conhecido como **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="f48d7-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="f48d7-137">Uma das contas do Exchange é marcada como a conta herdado do Exchange.</span><span class="sxs-lookup"><span data-stu-id="f48d7-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="f48d7-138">Normalmente, é a primeira conta adicionada ao perfil.</span><span class="sxs-lookup"><span data-stu-id="f48d7-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="f48d7-139">Cada chamada para abrir **pbGlobalProfileSectionGuid** é redirecionada para a seção global do Exchange da conta herdada.</span><span class="sxs-lookup"><span data-stu-id="f48d7-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="f48d7-140">As chamadas de modelo de objeto que interagem com a conta do Exchange não herdado também interagem com a conta herdado do Exchange.</span><span class="sxs-lookup"><span data-stu-id="f48d7-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="f48d7-141">O serviço Exchange herdado tem a propriedade **PR_EMSMDB_LEGACY** (0x3D18000B), que é definida como **true** na tabela de serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f48d7-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="f48d7-142">O **emsmdbUID** herdado também é carimbado na Seção de Perfil Global do Outlook do perfil como **PidTagExchangeProfileSectionId**.</span><span class="sxs-lookup"><span data-stu-id="f48d7-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="f48d7-143">O código escrito para dar suporte a várias contas do Exchange não deve ter que recuperar o **emsmdbUID** herdado porque ele deve obter o **emsmdbUID** correto, dependendo da conta com a que seu código está interagindo.</span><span class="sxs-lookup"><span data-stu-id="f48d7-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f48d7-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="f48d7-144">See also</span></span>



[<span data-ttu-id="f48d7-145">Usar várias contas do Exchange</span><span class="sxs-lookup"><span data-stu-id="f48d7-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="f48d7-146">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="f48d7-146">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

