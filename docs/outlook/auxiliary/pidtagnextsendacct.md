---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Especifica o accountsendstamp secundário da mensagem.
ms.openlocfilehash: 63d98382ff8a5a545cdb015c089c7b0a38926138
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766052"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="70534-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="70534-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="70534-104">Especifica o carimbo de conta secundária "Enviar" para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="70534-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="70534-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="70534-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70534-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="70534-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70534-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="70534-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="70534-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="70534-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70534-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="70534-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="70534-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="70534-110">Data type:</span></span>  <br/> |<span data-ttu-id="70534-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70534-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="70534-112">Área:</span><span class="sxs-lookup"><span data-stu-id="70534-112">Area:</span></span>  <br/> |<span data-ttu-id="70534-113">Aplicativo do Outlook</span><span class="sxs-lookup"><span data-stu-id="70534-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70534-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="70534-114">Remarks</span></span>

<span data-ttu-id="70534-115">Essa propriedade se aplica a um objeto de mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="70534-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="70534-116">Para uma mensagem recebida, o carimbo de data / conta secundária "Enviar" indica qual conta um encaminhamento ou uma resposta deve ser enviada com, se o encaminhamento e a resposta não pode ser enviada com a conta principal.</span><span class="sxs-lookup"><span data-stu-id="70534-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="70534-117">Para uma mensagem de saída, a conta secundária "Enviar" carimbo determina com qual conta para enviar a mensagem, se a mensagem não pode ser enviada com a conta principal.</span><span class="sxs-lookup"><span data-stu-id="70534-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="70534-118">Seu valor é o valor [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) da interface de [IOlkAccount](iolkaccount.md) da conta com a qual a mensagem está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="70534-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70534-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="70534-119">See also</span></span>

- [<span data-ttu-id="70534-120">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="70534-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="70534-121">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="70534-121">MAPI Properties</span></span>](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="70534-122">Propriedade canônica PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="70534-122">PidTagNextSendAcct Canonical Property</span></span>](http://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

