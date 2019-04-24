---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Especifica a saída de uma cópia de uma mensagem no servidor para uma conta POP.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326485"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="95564-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="95564-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="95564-104">Especifica a saída de uma cópia de uma mensagem no servidor para uma conta POP.</span><span class="sxs-lookup"><span data-stu-id="95564-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="95564-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="95564-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95564-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="95564-106">Identifier:</span></span>  <br/> |<span data-ttu-id="95564-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="95564-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="95564-108">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="95564-108">Property type:</span></span>  <br/> |<span data-ttu-id="95564-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="95564-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="95564-110">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="95564-110">Property tag:</span></span>  <br/> |<span data-ttu-id="95564-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="95564-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="95564-112">Acesso:</span><span class="sxs-lookup"><span data-stu-id="95564-112">Access:</span></span>  <br/> |<span data-ttu-id="95564-113">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95564-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95564-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="95564-114">Remarks</span></span>

<span data-ttu-id="95564-115">A tabela a seguir lista os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="95564-115">The following table lists the possible values.</span></span> <span data-ttu-id="95564-116">ConFira [constantes (API de gerenciamento de contas)](constants-account-management-api.md) para obter mais informações sobre as constantes.</span><span class="sxs-lookup"><span data-stu-id="95564-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="95564-117">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="95564-117">**Possible values**</span></span>|<span data-ttu-id="95564-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="95564-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95564-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="95564-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="95564-120">Deixa uma cópia da mensagem no servidor POP após o download da mensagem para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95564-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="95564-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="95564-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="95564-122">Remove a mensagem do servidor POP após o download para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95564-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="95564-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="95564-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="95564-124">Remove a mensagem do servidor POP somente depois que o usuário exclui a mensagem da pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="95564-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="95564-125">**GET_REMOVE_AFTER_DAYS** ( _UL_)</span><span class="sxs-lookup"><span data-stu-id="95564-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="95564-126">Obtém o número de dias após o qual a mensagem será removida do servidor POP.</span><span class="sxs-lookup"><span data-stu-id="95564-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="95564-127">**SET_REMOVE_AFTER_DAYS** ( _dias_)</span><span class="sxs-lookup"><span data-stu-id="95564-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="95564-128">Define o número de dias após o qual a mensagem será removida do servidor POP.</span><span class="sxs-lookup"><span data-stu-id="95564-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95564-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="95564-129">See also</span></span>

- [<span data-ttu-id="95564-130">Gerenciar o download de mensagens de contas POP3</span><span class="sxs-lookup"><span data-stu-id="95564-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="95564-131">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="95564-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

