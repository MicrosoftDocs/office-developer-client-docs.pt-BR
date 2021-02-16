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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327703"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="bdfde-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="bdfde-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="bdfde-104">Especifica o carimbo “send” de conta principal de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="bdfde-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bdfde-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="bdfde-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdfde-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bdfde-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bdfde-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bdfde-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="bdfde-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bdfde-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bdfde-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="bdfde-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="bdfde-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bdfde-110">Data type:</span></span>  <br/> |<span data-ttu-id="bdfde-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bdfde-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bdfde-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bdfde-112">Area:</span></span>  <br/> |<span data-ttu-id="bdfde-113">Conta</span><span class="sxs-lookup"><span data-stu-id="bdfde-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdfde-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdfde-114">Remarks</span></span>

<span data-ttu-id="bdfde-115">Essa propriedade se aplica a um objeto de mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="bdfde-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="bdfde-116">Para uma mensagem recebida, o carimbo “send” de conta principal indica com qual conta um encaminhamento ou uma resposta deve ser enviada.</span><span class="sxs-lookup"><span data-stu-id="bdfde-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="bdfde-117">Para uma mensagem de saída, ele determina com qual conta enviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="bdfde-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="bdfde-118">Seu valor é o valor de [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) da interface [IOlkAccount](iolkaccount.md) da conta com a qual a mensagem está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="bdfde-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bdfde-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdfde-119">See also</span></span>

- [<span data-ttu-id="bdfde-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="bdfde-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="bdfde-121">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bdfde-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="bdfde-122">Propriedade canônica PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="bdfde-122">PidTagPrimarySendAccount Canonical Property</span></span>](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

