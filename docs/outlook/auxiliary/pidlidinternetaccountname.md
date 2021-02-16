---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Retorna o nome de exibição da conta que entregou a mensagem.
ms.openlocfilehash: 2bd27cc7f868fb3f255a002ed70d0cb9b79516e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327682"
---
# <a name="pidlidinternetaccountname"></a><span data-ttu-id="1fc48-103">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="1fc48-103">PidLidInternetAccountName</span></span>

<span data-ttu-id="1fc48-104">Retorna o nome de exibição da conta que entregou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="1fc48-104">Returns the display name of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1fc48-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1fc48-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1fc48-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1fc48-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1fc48-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="1fc48-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="1fc48-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="1fc48-108">Property set:</span></span>  <br/> |<span data-ttu-id="1fc48-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="1fc48-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="1fc48-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1fc48-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1fc48-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="1fc48-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="1fc48-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1fc48-112">Data type:</span></span>  <br/> |<span data-ttu-id="1fc48-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1fc48-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1fc48-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1fc48-114">Area:</span></span>  <br/> |<span data-ttu-id="1fc48-115">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="1fc48-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fc48-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fc48-116">Remarks</span></span>

<span data-ttu-id="1fc48-117">Esta propriedade deve conter o mesmo valor retornado da propriedade da API de Gerenciamento de Conta [PROP_ACCT_NAME](prop_acct_name.md) da conta que entregou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="1fc48-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_NAME](prop_acct_name.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="1fc48-118">Os provedores de repositórios de mensagens expõem esta propriedade nomeada e [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) para que ocorram as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="1fc48-118">Message store providers expose this named property and [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="1fc48-119">Quando um usuário clica em **Responder a Todos** em uma mensagem de email, o Outlook remove o endereço de email associado à conta e marcado na mensagem da lista de destinatários da resposta.</span><span class="sxs-lookup"><span data-stu-id="1fc48-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="1fc48-120">Isso ocorre a menos que o endereço de email seja o remetente da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="1fc48-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="1fc48-121">Por padrão, o Outlook envia respostas e mensagens encaminhadas por meio da conta que está marcada na mensagem original.</span><span class="sxs-lookup"><span data-stu-id="1fc48-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="1fc48-122">Normalmente, o Gerenciador de Protocolo do Outlook entrega as mensagens, e o Outlook configura as propriedades **PidLidInternetAccountName** e **PidLidInternetAccountStamp** para indicar a conta que entregou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="1fc48-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="1fc48-123">No entanto, se um repositório de mensagens estiver firmemente acoplado a um transporte, o Outlook Protocol Manager não entregará as mensagens e o Outlook não poderá definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1fc48-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="1fc48-124">Nesse cenário, o Outlook chama a função [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1fc48-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="1fc48-125">Se o provedor de repositório de mensagens quiser expor essas propriedades nomeadas, deverá implementar **IMAPIProp::GetIDsFromNames** e retornar marcas de propriedade por meio do parâmetro de saída *lppPropTags* .</span><span class="sxs-lookup"><span data-stu-id="1fc48-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="1fc48-126">O Outlook, em seguida, poderá chamar o método [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) usando essas marcas de propriedade, e o provedor de armazenamento de mensagens pode retornar o nome da conta e o carimbo da conta desejada.</span><span class="sxs-lookup"><span data-stu-id="1fc48-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="1fc48-127">Para dar suporte a essas propriedades nomeadas, os provedores de repositórios devem esperar para usar o Outlook **IMAPIProp::GetIDsFromNames** para obter a marca de propriedade para esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="1fc48-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="1fc48-128">O Outlook especifica os seguintes valores para a estrutura [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx), que corresponde a esta propriedade nomeada, que é passada como parte da matriz apontada pelo parâmetro de entrada *lppPropNames* de **IMAPIProp::GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="1fc48-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1fc48-129">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="1fc48-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="1fc48-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="1fc48-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="1fc48-131">ulKind:</span><span class="sxs-lookup"><span data-stu-id="1fc48-131">ulKind:</span></span>  <br/> |<span data-ttu-id="1fc48-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="1fc48-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="1fc48-133">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="1fc48-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="1fc48-134">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="1fc48-134">dispidInetAcctName</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1fc48-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fc48-135">See also</span></span>

- [<span data-ttu-id="1fc48-136">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="1fc48-136">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="1fc48-137">Constantes (PI de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="1fc48-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="1fc48-138">Propriedade canônica PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="1fc48-138">PidLidInternetAccountName Canonical Property</span></span>](https://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

