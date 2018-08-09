---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Especifica o accountsendstamp principal de uma mensagem.
ms.openlocfilehash: f94ac104a77e8400909dc06db44ce8ca03e4653f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766046"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="13e08-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="13e08-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="13e08-104">Especifica o carimbo de "Enviar" da conta principal para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="13e08-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="13e08-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="13e08-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13e08-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="13e08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13e08-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="13e08-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="13e08-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="13e08-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13e08-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="13e08-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="13e08-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="13e08-110">Data type:</span></span>  <br/> |<span data-ttu-id="13e08-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13e08-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="13e08-112">Área:</span><span class="sxs-lookup"><span data-stu-id="13e08-112">Area:</span></span>  <br/> |<span data-ttu-id="13e08-113">Conta</span><span class="sxs-lookup"><span data-stu-id="13e08-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13e08-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="13e08-114">Remarks</span></span>

<span data-ttu-id="13e08-115">Essa propriedade se aplica a um objeto de mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="13e08-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="13e08-116">Para uma mensagem recebida, o carimbo de "Enviar" da conta principal indica qual conta um encaminhamento ou uma resposta deve ser enviada com.</span><span class="sxs-lookup"><span data-stu-id="13e08-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="13e08-117">Para uma mensagem de saída, ele determina qual conta para enviar a mensagem com.</span><span class="sxs-lookup"><span data-stu-id="13e08-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="13e08-118">Seu valor é o valor [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) da interface de [IOlkAccount](iolkaccount.md) da conta com a qual a mensagem está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="13e08-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13e08-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="13e08-119">See also</span></span>

- [<span data-ttu-id="13e08-120">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="13e08-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="13e08-121">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="13e08-121">MAPI Properties</span></span>](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="13e08-122">Propriedade canônica PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="13e08-122">PidTagPrimarySendAccount Canonical Property</span></span>](http://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

