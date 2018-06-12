---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Retorna o carimbo da conta da conta que entregar a mensagem.
ms.openlocfilehash: ba54bffb60a05a3b4a1ff30519960740af93ebd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766044"
---
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="464a8-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="464a8-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="464a8-104">Retorna o carimbo da conta da conta que entregar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="464a8-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="464a8-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="464a8-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="464a8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="464a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="464a8-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="464a8-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="464a8-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="464a8-108">Property set:</span></span>  <br/> |<span data-ttu-id="464a8-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="464a8-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="464a8-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="464a8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="464a8-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="464a8-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="464a8-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="464a8-112">Data type:</span></span>  <br/> |<span data-ttu-id="464a8-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="464a8-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="464a8-114">Área:</span><span class="sxs-lookup"><span data-stu-id="464a8-114">Area:</span></span>  <br/> |<span data-ttu-id="464a8-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="464a8-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="464a8-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="464a8-116">Remarks</span></span>

<span data-ttu-id="464a8-117">Essa propriedade deve conter o mesmo valor que é retornado da propriedade API de gerenciamento de conta [PROP_ACCT_STAMP](prop_acct_stamp.md) para a conta que entregar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="464a8-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="464a8-118">Provedores de armazenamento de mensagem exponham essa propriedade nomeada e [PidLidInternetAccountName](pidlidinternetaccountname.md) para que ocorrem as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="464a8-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="464a8-119">Quando um usuário clica **responder a todos** em uma mensagem de email, o Outlook remove o endereço de email que está associado à conta e é marcado em mensagem da lista de destinatários da resposta.</span><span class="sxs-lookup"><span data-stu-id="464a8-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="464a8-120">Esse comportamento ocorre, a menos que esse endereço de email é o remetente da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="464a8-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="464a8-121">Por padrão, o Outlook envia respostas e encaminhadas através da conta que é marcada na mensagem original.</span><span class="sxs-lookup"><span data-stu-id="464a8-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="464a8-122">Em geral, o gerente de protocolo do Outlook entrega de mensagens e Outlook define as propriedades **PidLidInternetAccountName** e **PidLidInternetAccountStamp** para indicar a conta que entregar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="464a8-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="464a8-123">No entanto, se um armazenamento de mensagens está intimamente ligado com um transporte, o gerente de protocolo do Outlook não entregar mensagens e o Outlook não pode definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="464a8-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="464a8-124">Neste cenário, o Outlook chama a função [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="464a8-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="464a8-125">Se o provedor de armazenamento de mensagem deseja expor essas propriedades nomeadas, ele deve implementar **IMAPIProp::GetIDsFromNames** e retornar as marcas de propriedade por meio do parâmetro de saída *lppPropTags* .</span><span class="sxs-lookup"><span data-stu-id="464a8-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="464a8-126">Outlook, chame o método [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) usando essas marcas da propriedade e o provedor de armazenamento de mensagens pode retornar o nome da conta e o carimbo da conta desejada.</span><span class="sxs-lookup"><span data-stu-id="464a8-126">Outlook can then call the [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="464a8-127">Para oferecer suporte a essas propriedades nomeadas, provedores de armazenamento devem esperar que o Outlook para usar **IMAPIProp::GetIDsFromNames** para obter a marca de propriedade para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="464a8-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="464a8-128">Outlook Especifica os seguintes valores para a estrutura [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) que corresponde a essa propriedade nomeada, que é passada como parte da matriz apontada pelo parâmetro de entrada *lppPropNames* do **IMAPIProp::GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="464a8-128">Outlook specifies the following values for the [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="464a8-129">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="464a8-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="464a8-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="464a8-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="464a8-131">ulKind:</span><span class="sxs-lookup"><span data-stu-id="464a8-131">ulKind:</span></span>  <br/> |<span data-ttu-id="464a8-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="464a8-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="464a8-133">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="464a8-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="464a8-134">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="464a8-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="464a8-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="464a8-135">See also</span></span>

- [<span data-ttu-id="464a8-136">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="464a8-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="464a8-137">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="464a8-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="464a8-138">Propriedade canônico de PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="464a8-138">PidLidInternetAccountStamp Canonical Property</span></span>](http://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

