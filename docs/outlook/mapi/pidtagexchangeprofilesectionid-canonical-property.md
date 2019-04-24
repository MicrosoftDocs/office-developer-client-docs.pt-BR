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
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="3e0ad-103">Propriedade canônica PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="3e0ad-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="3e0ad-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e0ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e0ad-105">Contém um GUID gerado dinamicamente usado para determinar uma conta quando você estiver usando várias contas do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e0ad-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3e0ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e0ad-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="3e0ad-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="3e0ad-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3e0ad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3e0ad-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="3e0ad-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="3e0ad-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3e0ad-110">Data type:</span></span>  <br/> |<span data-ttu-id="3e0ad-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3e0ad-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3e0ad-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3e0ad-112">Area:</span></span>  <br/> |<span data-ttu-id="3e0ad-113">Várias contas do Exchange</span><span class="sxs-lookup"><span data-stu-id="3e0ad-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e0ad-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e0ad-114">Remarks</span></span>

<span data-ttu-id="3e0ad-115">O Microsoft Outlook 2010 e o Microsoft Outlook 2013 dão suporte a várias contas do Exchange, em vez de uma única conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="3e0ad-116">Para acomodar várias contas do Exchange, o layout do perfil MAPI foi alterado.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="3e0ad-117">No Microsoft Office Outlook 2007 e anteriores, os perfis continham uma seção de perfil fixo dedicada às configurações do Exchange, como nome do servidor, nome de usuário e arquivo de pasta offline (. ost).</span><span class="sxs-lookup"><span data-stu-id="3e0ad-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="3e0ad-118">alocações.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-118">location.</span></span> <span data-ttu-id="3e0ad-119">Essas configurações foram identificadas usando um identificador exclusivo, a propriedade **pbGlobalProfileSectionGuid** .</span><span class="sxs-lookup"><span data-stu-id="3e0ad-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="3e0ad-120">A seção usada para as configurações do Exchange é chamada de seção de perfil global do Exchange.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="3e0ad-121">Um local de seção de perfil fixo não é mais suficiente para acomodar várias contas do Exchange.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="3e0ad-122">Em vez disso, para cada conta do Exchange em seu perfil, existe uma seção que é dedicada às configurações da conta.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="3e0ad-123">A nova seção usada para as configurações do Exchange é identificada pelo identificador exclusivo **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="3e0ad-124">Na seção perfil de serviço de mensagens da conta do Exchange, você pode encontrar uma propriedade que contenha um GUID gerado dinamicamente no momento em que a conta é criada.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="3e0ad-125">Este GUID é armazenado na propriedade **PidTagExchangeProfileSectionId** .</span><span class="sxs-lookup"><span data-stu-id="3e0ad-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="3e0ad-126">Repositórios de mensagens e contêineres de catálogo de endereços expõem uma propriedade para determinar a conta do Exchange à qual pertencem.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="3e0ad-127">Acessível na tabela de serviços de mensagem, cada serviço do Exchange expõe essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="3e0ad-128">Você pode recuperar essa propriedade por meio de uma chamada a [IMAPIProp::](imapiprop-getprops.md) GetProps no **PidTagExchangeProfileSectionId** após a consulta para qualquer uma das seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="3e0ad-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="3e0ad-129">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3e0ad-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="3e0ad-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3e0ad-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="3e0ad-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3e0ad-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="3e0ad-132">Se o objeto não estiver associado ao Exchange, a chamada retornará **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="3e0ad-133">Você pode restringir os contêineres em um **PidTagExchangeProfileSectionId** ao exibir o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="3e0ad-134">Depois de ter um contêiner aberto, você pode consultar o **emsmdbUID** dele.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="3e0ad-135">Também vale a pena observar que, se um destinatário tiver sido selecionado de um catálogo de endereços do Exchange, o destinatário também terá o **PidTagExchangeProfileSectionId** em sua lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3e0ad-136">Em todos os exemplos de código e cabeçalhos de função, esse GUID é conhecido como **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="3e0ad-137">Uma das contas do Exchange é marcada como a conta herdada do Exchange.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="3e0ad-138">Normalmente, é a primeira conta adicionada ao perfil.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="3e0ad-139">Cada chamada para abrir **pbGlobalProfileSectionGuid** é redirecionada para a seção global do Exchange da conta herdada.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="3e0ad-140">As chamadas de modelo de objeto que interagem com a conta não herdada do Exchange também interagem com a conta herdada do Exchange.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="3e0ad-141">O serviço do Exchange herdado tem a propriedade **PR_EMSMDB_LEGACY** (0x3D18000B), que é definida como **true** na tabela de serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="3e0ad-142">O **emsmdbUID** herdado também está marcado na seção perfil global do Outlook do perfil como **PidTagExchangeProfileSectionId**.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="3e0ad-143">O código escrito para dar suporte a várias contas do Exchange não deve ter que recuperar o **emsmdbUID** herdado porque deve obter o **emsmdbUID**correto, dependendo da conta com a qual seu código está interagindo.</span><span class="sxs-lookup"><span data-stu-id="3e0ad-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e0ad-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e0ad-144">See also</span></span>



[<span data-ttu-id="3e0ad-145">Usar várias contas do Exchange</span><span class="sxs-lookup"><span data-stu-id="3e0ad-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="3e0ad-146">Como abrir a seção de perfil global</span><span class="sxs-lookup"><span data-stu-id="3e0ad-146">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

