---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Especifica o tipo de conexão criptografada a ser usada para uma conta SMTP.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328326"
---
# <a name="propsmtpsecureconnection"></a><span data-ttu-id="18443-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="18443-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="18443-104">Especifica o tipo de conexão criptografada a ser usada para uma conta SMTP.</span><span class="sxs-lookup"><span data-stu-id="18443-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="18443-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="18443-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18443-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="18443-106">Identifier:</span></span>  <br/> |<span data-ttu-id="18443-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="18443-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="18443-108">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="18443-108">Property type:</span></span>  <br/> |<span data-ttu-id="18443-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="18443-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="18443-110">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="18443-110">Property tag:</span></span>  <br/> |<span data-ttu-id="18443-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="18443-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="18443-112">Acesso:</span><span class="sxs-lookup"><span data-stu-id="18443-112">Access:</span></span>  <br/> |<span data-ttu-id="18443-113">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18443-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18443-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="18443-114">Remarks</span></span>

<span data-ttu-id="18443-115">O valor pode ser uma das seguintes constantes.</span><span class="sxs-lookup"><span data-stu-id="18443-115">The value can be one of the following constants.</span></span> <span data-ttu-id="18443-116">ConFira [constantes (API de gerenciamento de contas)](constants-account-management-api.md) para seus valores.</span><span class="sxs-lookup"><span data-stu-id="18443-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="18443-117">**Constants**</span><span class="sxs-lookup"><span data-stu-id="18443-117">**Constants**</span></span>|<span data-ttu-id="18443-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="18443-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18443-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="18443-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="18443-120">Não use nenhuma criptografia.</span><span class="sxs-lookup"><span data-stu-id="18443-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="18443-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="18443-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="18443-122">Use a criptografia SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="18443-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="18443-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="18443-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="18443-124">Use o protocolo de autenticação e criptografia TLS (Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="18443-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="18443-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="18443-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="18443-126">Detectar e usar automaticamente o método de criptografia suportado pelo servidor de email.</span><span class="sxs-lookup"><span data-stu-id="18443-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18443-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="18443-127">See also</span></span>

- [<span data-ttu-id="18443-128">Gerenciar o download de mensagens de contas POP3</span><span class="sxs-lookup"><span data-stu-id="18443-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="18443-129">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="18443-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

