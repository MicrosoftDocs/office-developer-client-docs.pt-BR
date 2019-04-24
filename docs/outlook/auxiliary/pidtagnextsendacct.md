---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Especifica o accountsendstamp secundário de uma mensagem.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327710"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="1c940-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="1c940-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="1c940-104">Especifica o carimbo “send” de conta secundário de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1c940-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1c940-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1c940-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c940-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1c940-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c940-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="1c940-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="1c940-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1c940-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c940-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="1c940-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="1c940-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1c940-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c940-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1c940-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1c940-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1c940-112">Area:</span></span>  <br/> |<span data-ttu-id="1c940-113">Aplicativo do Outlook</span><span class="sxs-lookup"><span data-stu-id="1c940-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c940-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c940-114">Remarks</span></span>

<span data-ttu-id="1c940-115">Essa propriedade se aplica a um objeto de mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="1c940-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="1c940-116">Para uma mensagem recebida, o carimbo “send” de conta principal indica com qual conta será preciso enviar um encaminhamento ou uma resposta se não puder ser enviado com a conta principal.</span><span class="sxs-lookup"><span data-stu-id="1c940-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="1c940-117">Para uma mensagem de saída, o carimbo “send” de conta secundária determina com qual conta será preciso enviar a mensagem se não puder ser enviada com a conta principal.</span><span class="sxs-lookup"><span data-stu-id="1c940-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="1c940-118">Seu valor é o valor de [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) da interface [IOlkAccount](iolkaccount.md) da conta com a qual a mensagem está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="1c940-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1c940-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c940-119">See also</span></span>

- [<span data-ttu-id="1c940-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="1c940-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="1c940-121">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1c940-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="1c940-122">Propriedade canônica PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="1c940-122">PidTagNextSendAcct Canonical Property</span></span>](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

