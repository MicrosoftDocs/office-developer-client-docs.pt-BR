---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Especifica o tipo de conexão criptografada a ser usado para uma conta de SMTP.
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766071"
---
# <a name="propsmtpsecureconnection"></a><span data-ttu-id="d8a9d-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="d8a9d-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="d8a9d-104">Especifica o tipo de conexão criptografada a ser usado para uma conta de SMTP.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d8a9d-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d8a9d-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8a9d-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d8a9d-106">Identifier:</span></span>  <br/> |<span data-ttu-id="d8a9d-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="d8a9d-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="d8a9d-108">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d8a9d-108">Property type:</span></span>  <br/> |<span data-ttu-id="d8a9d-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="d8a9d-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="d8a9d-110">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d8a9d-110">Property tag:</span></span>  <br/> |<span data-ttu-id="d8a9d-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="d8a9d-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="d8a9d-112">Access:</span><span class="sxs-lookup"><span data-stu-id="d8a9d-112">Access:</span></span>  <br/> |<span data-ttu-id="d8a9d-113">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8a9d-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8a9d-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="d8a9d-114">Remarks</span></span>

<span data-ttu-id="d8a9d-115">O valor pode ser uma das constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-115">The value can be one of the following constants.</span></span> <span data-ttu-id="d8a9d-116">Consulte [constantes (API de gerenciamento de conta)](constants-account-management-api.md) para seus valores.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="d8a9d-117">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="d8a9d-117">**Constants**</span></span>|<span data-ttu-id="d8a9d-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8a9d-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8a9d-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="d8a9d-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="d8a9d-120">Não use qualquer criptografia.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="d8a9d-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="d8a9d-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="d8a9d-122">Use a criptografia de camada de soquete seguro (SSL).</span><span class="sxs-lookup"><span data-stu-id="d8a9d-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="d8a9d-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="d8a9d-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="d8a9d-124">Use o protocolo de autenticação e criptografia de segurança de camada de transporte (TLS).</span><span class="sxs-lookup"><span data-stu-id="d8a9d-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="d8a9d-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="d8a9d-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="d8a9d-126">Detectar automaticamente e usar o método de criptografia suportado pelo servidor de email.</span><span class="sxs-lookup"><span data-stu-id="d8a9d-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8a9d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8a9d-127">See also</span></span>

- [<span data-ttu-id="d8a9d-128">Gerenciando mensagem downloads para contas POP3</span><span class="sxs-lookup"><span data-stu-id="d8a9d-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="d8a9d-129">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="d8a9d-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

