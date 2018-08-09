---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Especifica o método de autenticação a ser usado para a conta de SMTP.
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766075"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="2af2f-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="2af2f-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="2af2f-104">Especifica o método de autenticação a ser usado para a conta de SMTP.</span><span class="sxs-lookup"><span data-stu-id="2af2f-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2af2f-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2af2f-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2af2f-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2af2f-106">Identifier:</span></span>  <br/> |<span data-ttu-id="2af2f-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="2af2f-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="2af2f-108">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="2af2f-108">Property type:</span></span>  <br/> |<span data-ttu-id="2af2f-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="2af2f-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="2af2f-110">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="2af2f-110">Property tag:</span></span>  <br/> |<span data-ttu-id="2af2f-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="2af2f-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="2af2f-112">Access:</span><span class="sxs-lookup"><span data-stu-id="2af2f-112">Access:</span></span>  <br/> |<span data-ttu-id="2af2f-113">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2af2f-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2af2f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2af2f-114">Remarks</span></span>

<span data-ttu-id="2af2f-115">O valor é uma bitmask das seguintes constantes.</span><span class="sxs-lookup"><span data-stu-id="2af2f-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="2af2f-116">Consulte [constantes (API de gerenciamento de conta)](constants-account-management-api.md) para seus valores.</span><span class="sxs-lookup"><span data-stu-id="2af2f-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="2af2f-117">**SMTP_AUTH_SAME_AS_POP** significa usando as mesmas credenciais como meu servidor de email de entrada, conforme fornecido pela [PROP_INET_USER](prop_inet_user.md) e [PROP_INET_PASSWORD](prop_inet_password.md).</span><span class="sxs-lookup"><span data-stu-id="2af2f-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="2af2f-118">**SMTP_AUTH_USER_PASS** significa utilizando as credenciais conforme fornecido pela [PROP_SMTP_USER](prop_smtp_user.md) e [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span><span class="sxs-lookup"><span data-stu-id="2af2f-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="2af2f-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** significa solicitando que o usuário para fazer logon no servidor de email de entrada antes de enviar email.</span><span class="sxs-lookup"><span data-stu-id="2af2f-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2af2f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="2af2f-120">See also</span></span>

- [<span data-ttu-id="2af2f-121">Gerenciar o download de mensagens de contas POP3</span><span class="sxs-lookup"><span data-stu-id="2af2f-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="2af2f-122">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="2af2f-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

