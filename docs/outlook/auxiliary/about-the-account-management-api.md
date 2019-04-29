---
title: Sobre a API de gerenciamento de contas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'A API de gerenciamento de contas fornece acesso a informações de conta e dá suporte a notificações de alterações de conta. Como clientes desta API, os provedores de email fazem o seguinte:'
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426246"
---
# <a name="about-the-account-management-api"></a><span data-ttu-id="dd33d-104">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="dd33d-104">About the Account Management API</span></span>

<span data-ttu-id="dd33d-105">A API de gerenciamento de contas fornece acesso a informações de conta e dá suporte a notificações de alterações de conta.</span><span class="sxs-lookup"><span data-stu-id="dd33d-105">The Account Management API provides access to account information and supports notifications of account changes.</span></span> <span data-ttu-id="dd33d-106">Como clientes desta API, os provedores de email fazem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dd33d-106">As clients of this API, mail providers do the following:</span></span>
  
1. <span data-ttu-id="dd33d-107">Use o [IOlkAccountManager](iolkaccountmanager.md) para gerenciar o acesso a contas e configurar notificações sobre alterações de conta.</span><span class="sxs-lookup"><span data-stu-id="dd33d-107">Use [IOlkAccountManager](iolkaccountmanager.md) to manage access to accounts and set up notifications about account changes.</span></span> 
    
2. <span data-ttu-id="dd33d-108">Implementar e usar o [IOlkAccountNotify](iolkaccountnotify.md) para enviar notificações sobre alterações de conta.</span><span class="sxs-lookup"><span data-stu-id="dd33d-108">Implement and use [IOlkAccountNotify](iolkaccountnotify.md) to send notifications about account changes.</span></span> 
    
3. <span data-ttu-id="dd33d-109">Use [IOlkEnum](iolkenum.md) para enumerar contas.</span><span class="sxs-lookup"><span data-stu-id="dd33d-109">Use [IOlkEnum](iolkenum.md) to enumerate accounts.</span></span> 
    
4. <span data-ttu-id="dd33d-110">Use o [IOlkAccount](iolkaccount.md) para obter e definir propriedades e outras informações sobre uma conta.</span><span class="sxs-lookup"><span data-stu-id="dd33d-110">Use [IOlkAccount](iolkaccount.md) to get and set properties and other information about an account.</span></span> <span data-ttu-id="dd33d-111">Os clientes obtêm essa interface por meio do [IOlkAccountManager:: FindAccount](iolkaccountmanager-findaccount.md) ou [IOlkEnum:: GetNext](iolkenum-getnext.md) para acessar uma conta individual.</span><span class="sxs-lookup"><span data-stu-id="dd33d-111">Clients obtain this interface through [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) or [IOlkEnum::GetNext](iolkenum-getnext.md) to access an individual account.</span></span> 
    
5. <span data-ttu-id="dd33d-112">Implementar e usar o [IOlkAccountHelper](iolkaccounthelper.md) para fornecer a funcionalidade auxiliar do gerente de contas, incluindo obter o nome do perfil da conta e a sessão MAPI atual.</span><span class="sxs-lookup"><span data-stu-id="dd33d-112">Implement and use [IOlkAccountHelper](iolkaccounthelper.md) to provide the account manager helper functionality, including getting an account's profile name and the current MAPI session.</span></span> 
    
6. <span data-ttu-id="dd33d-113">Implementar e usar o [IOlkErrorUnknown](iolkerrorunknown.md) para fornecer informações adicionais sobre um erro no **IOlkAccountManager**, **IOlkAccountNotify**e **IOlkAccount**.</span><span class="sxs-lookup"><span data-stu-id="dd33d-113">Implement and use [IOlkErrorUnknown](iolkerrorunknown.md) to provide extra information about an error in **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 

##  <a name="account-management-api-components"></a><span data-ttu-id="dd33d-114">Componentes da API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="dd33d-114">Account Management API components</span></span>

<span data-ttu-id="dd33d-115">A API de gerenciamento de contas fornece as seguintes definições, tipos de dados, interfaces, propriedades nomeadas e propriedades.</span><span class="sxs-lookup"><span data-stu-id="dd33d-115">The Account Management API provides the following definitions, data types, interfaces, named properties, and properties.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="dd33d-116">Definições</span><span class="sxs-lookup"><span data-stu-id="dd33d-116">Definitions</span></span>
  
- [<span data-ttu-id="dd33d-117">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="dd33d-117">Constants (Account management API)</span></span>](constants-account-management-api.md)
    
### <a name="data-types"></a><span data-ttu-id="dd33d-118">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="dd33d-118">Data types</span></span>
  
- [<span data-ttu-id="dd33d-119">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="dd33d-119">ACCT_BIN</span></span>](acct_bin.md)
    
- [<span data-ttu-id="dd33d-120">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="dd33d-120">ACCT_VARIANT</span></span>](acct_variant.md)
    
### <a name="interfaces"></a><span data-ttu-id="dd33d-121">Interfaces</span><span class="sxs-lookup"><span data-stu-id="dd33d-121">Interfaces</span></span>
  
- [<span data-ttu-id="dd33d-122">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="dd33d-122">IOlkAccount</span></span>](iolkaccount.md)
    
- [<span data-ttu-id="dd33d-123">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="dd33d-123">IOlkAccountHelper</span></span>](iolkaccounthelper.md)
    
- [<span data-ttu-id="dd33d-124">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="dd33d-124">IOlkAccountManager</span></span>](iolkaccountmanager.md)
    
- [<span data-ttu-id="dd33d-125">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="dd33d-125">IOlkAccountNotify</span></span>](iolkaccountnotify.md)
    
- [<span data-ttu-id="dd33d-126">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="dd33d-126">IOlkEnum</span></span>](iolkenum.md)
    
- [<span data-ttu-id="dd33d-127">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="dd33d-127">IOlkErrorUnknown</span></span>](iolkerrorunknown.md)
    
### <a name="named-properties"></a><span data-ttu-id="dd33d-128">Propriedades nomeadas</span><span class="sxs-lookup"><span data-stu-id="dd33d-128">Named properties</span></span>
  
- [<span data-ttu-id="dd33d-129">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="dd33d-129">PidLidInternetAccountName</span></span>](pidlidinternetaccountname.md)
    
- [<span data-ttu-id="dd33d-130">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="dd33d-130">PidLidInternetAccountStamp</span></span>](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a><span data-ttu-id="dd33d-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dd33d-131">Properties</span></span>
  
- [<span data-ttu-id="dd33d-132">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="dd33d-132">PidTagNextSendAcct</span></span>](pidtagnextsendacct.md)
    
- [<span data-ttu-id="dd33d-133">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="dd33d-133">PidTagPrimarySendAccount</span></span>](pidtagprimarysendaccount.md)
    
- [<span data-ttu-id="dd33d-134">PROP_ACCT_DELIVERY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="dd33d-134">PROP_ACCT_DELIVERY_FOLDER</span></span>](prop_acct_delivery_folder.md)
    
- [<span data-ttu-id="dd33d-135">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="dd33d-135">PROP_ACCT_DELIVERY_STORE</span></span>](prop_acct_delivery_store.md)
    
- [<span data-ttu-id="dd33d-136">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="dd33d-136">PROP_ACCT_ID</span></span>](prop_acct_id.md)
    
- [<span data-ttu-id="dd33d-137">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="dd33d-137">PROP_ACCT_IS_EXCH</span></span>](prop_acct_is_exch.md)
    
- [<span data-ttu-id="dd33d-138">PROP_ACCT_NAME</span><span class="sxs-lookup"><span data-stu-id="dd33d-138">PROP_ACCT_NAME</span></span>](prop_acct_name.md)
    
- [<span data-ttu-id="dd33d-139">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="dd33d-139">PROP_ACCT_PREFERENCES_UID</span></span>](prop_acct_preferences_uid.md)
    
- [<span data-ttu-id="dd33d-140">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="dd33d-140">PROP_ACCT_SEND_STAMP</span></span>](prop_acct_send_stamp.md)
    
- [<span data-ttu-id="dd33d-141">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="dd33d-141">PROP_ACCT_SENTITEMS_EID</span></span>](prop_acct_sentitems_eid.md)
    
- [<span data-ttu-id="dd33d-142">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="dd33d-142">PROP_ACCT_STAMP</span></span>](prop_acct_stamp.md)
    
- [<span data-ttu-id="dd33d-143">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="dd33d-143">PROP_ACCT_USER_EMAIL_ADDR</span></span>](prop_acct_user_email_addr.md)
    
- [<span data-ttu-id="dd33d-144">PROP_ACCT_USER_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="dd33d-144">PROP_ACCT_USER_DISPLAY_NAME</span></span>](prop_acct_user_display_name.md)
    
- [<span data-ttu-id="dd33d-145">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="dd33d-145">PROP_MAPI_EMSMDB_UID</span></span>](prop_mapi_emsmdb_uid.md)
    
- [<span data-ttu-id="dd33d-146">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="dd33d-146">PROP_MAPI_IDENTITY_ENTRYID</span></span>](prop_mapi_identity_entryid.md)
    
- [<span data-ttu-id="dd33d-147">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="dd33d-147">PROP_MAPI_TRANSPORT_FLAGS</span></span>](prop_mapi_transport_flags.md)
    

