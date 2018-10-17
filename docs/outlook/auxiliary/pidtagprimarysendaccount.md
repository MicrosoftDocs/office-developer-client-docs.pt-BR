---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Especifica o accountsendstamp principal de uma mensagem.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394080"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="2a211-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="2a211-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="2a211-104">Especifica o carimbo “send” de conta principal de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="2a211-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2a211-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2a211-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a211-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2a211-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a211-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2a211-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="2a211-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2a211-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a211-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="2a211-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="2a211-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2a211-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a211-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2a211-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2a211-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2a211-112">Area:</span></span>  <br/> |<span data-ttu-id="2a211-113">Conta</span><span class="sxs-lookup"><span data-stu-id="2a211-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a211-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a211-114">Remarks</span></span>

<span data-ttu-id="2a211-115">Essa propriedade se aplica a um objeto de mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="2a211-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="2a211-116">Para uma mensagem recebida, o carimbo “send” de conta principal indica com qual conta um encaminhamento ou uma resposta deve ser enviada.</span><span class="sxs-lookup"><span data-stu-id="2a211-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="2a211-117">Para uma mensagem de saída, ele determina com qual conta enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="2a211-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="2a211-118">Seu valor é o valor de [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) da interface [IOlkAccount](iolkaccount.md) da conta com a qual a mensagem está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="2a211-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a211-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a211-119">See also</span></span>

- [<span data-ttu-id="2a211-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="2a211-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="2a211-121">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2a211-121">MAPI Named Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="2a211-122">Propriedade canônica PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="2a211-122">PidTagPrimarySendAccount Canonical Property</span></span>](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

