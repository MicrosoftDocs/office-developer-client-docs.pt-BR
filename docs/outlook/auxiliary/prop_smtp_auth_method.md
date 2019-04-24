---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Especifica o método de autenticação a ser usado para a conta SMTP.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326499"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="d27e7-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="d27e7-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="d27e7-104">Especifica o método de autenticação a ser usado para a conta SMTP.</span><span class="sxs-lookup"><span data-stu-id="d27e7-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d27e7-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d27e7-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d27e7-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d27e7-106">Identifier:</span></span>  <br/> |<span data-ttu-id="d27e7-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="d27e7-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="d27e7-108">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d27e7-108">Property type:</span></span>  <br/> |<span data-ttu-id="d27e7-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="d27e7-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="d27e7-110">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d27e7-110">Property tag:</span></span>  <br/> |<span data-ttu-id="d27e7-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="d27e7-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="d27e7-112">Acesso:</span><span class="sxs-lookup"><span data-stu-id="d27e7-112">Access:</span></span>  <br/> |<span data-ttu-id="d27e7-113">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d27e7-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d27e7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d27e7-114">Remarks</span></span>

<span data-ttu-id="d27e7-115">O valor é uma bitmask das constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="d27e7-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="d27e7-116">ConFira [constantes (API de gerenciamento de contas)](constants-account-management-api.md) para seus valores.</span><span class="sxs-lookup"><span data-stu-id="d27e7-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="d27e7-117">**SMTP_AUTH_SAME_AS_POP** significa usar as mesmas credenciais que meu servidor de email de entrada, conforme fornecido por [PROP_INET_USER](prop_inet_user.md) e [PROP_INET_PASSWORD](prop_inet_password.md).</span><span class="sxs-lookup"><span data-stu-id="d27e7-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="d27e7-118">**SMTP_AUTH_USER_PASS** significa usar as credenciais conforme fornecido por [PROP_SMTP_USER](prop_smtp_user.md) e [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span><span class="sxs-lookup"><span data-stu-id="d27e7-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="d27e7-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** significa solicitar que o usuário faça logon no servidor de email de entrada antes de enviar email.</span><span class="sxs-lookup"><span data-stu-id="d27e7-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d27e7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d27e7-120">See also</span></span>

- [<span data-ttu-id="d27e7-121">Gerenciar o download de mensagens de contas POP3</span><span class="sxs-lookup"><span data-stu-id="d27e7-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="d27e7-122">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="d27e7-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

