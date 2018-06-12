---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Especifica a deixar uma cópia de uma mensagem no servidor para uma conta POP.
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766062"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="82f31-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="82f31-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="82f31-104">Especifica a deixar uma cópia de uma mensagem no servidor para uma conta POP.</span><span class="sxs-lookup"><span data-stu-id="82f31-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="82f31-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="82f31-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82f31-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="82f31-106">Identifier:</span></span>  <br/> |<span data-ttu-id="82f31-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="82f31-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="82f31-108">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="82f31-108">Property type:</span></span>  <br/> |<span data-ttu-id="82f31-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="82f31-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="82f31-110">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="82f31-110">Property tag:</span></span>  <br/> |<span data-ttu-id="82f31-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="82f31-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="82f31-112">Access:</span><span class="sxs-lookup"><span data-stu-id="82f31-112">Access:</span></span>  <br/> |<span data-ttu-id="82f31-113">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82f31-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82f31-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="82f31-114">Remarks</span></span>

<span data-ttu-id="82f31-115">A tabela a seguir lista os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="82f31-115">The following table lists the possible values.</span></span> <span data-ttu-id="82f31-116">Consulte [constantes (API de gerenciamento de conta)](constants-account-management-api.md) para obter mais informações sobre as constantes.</span><span class="sxs-lookup"><span data-stu-id="82f31-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="82f31-117">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="82f31-117">**Possible values**</span></span>|<span data-ttu-id="82f31-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="82f31-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="82f31-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="82f31-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="82f31-120">Deixar uma cópia da mensagem no servidor POP depois de baixar a mensagem a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82f31-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="82f31-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="82f31-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="82f31-122">Remove a mensagem do servidor POP após fazer o download em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82f31-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="82f31-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="82f31-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="82f31-124">Remove a mensagem do servidor POP somente depois que o usuário excluir a mensagem da pasta Itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="82f31-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="82f31-125">**GET_REMOVE_AFTER_DAYS** ( _ul_)</span><span class="sxs-lookup"><span data-stu-id="82f31-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="82f31-126">Obtém o número de dias após o qual a mensagem será removida do servidor POP.</span><span class="sxs-lookup"><span data-stu-id="82f31-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="82f31-127">**SET_REMOVE_AFTER_DAYS** ( _dias_)</span><span class="sxs-lookup"><span data-stu-id="82f31-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="82f31-128">Define o número de dias após o qual a mensagem será removida do servidor POP.</span><span class="sxs-lookup"><span data-stu-id="82f31-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82f31-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="82f31-129">See also</span></span>

- [<span data-ttu-id="82f31-130">Gerenciando mensagem downloads para contas POP3</span><span class="sxs-lookup"><span data-stu-id="82f31-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="82f31-131">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="82f31-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

