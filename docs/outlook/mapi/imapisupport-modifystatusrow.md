---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316636"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="42ffa-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="42ffa-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="42ffa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42ffa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42ffa-105">Modifica a tabela status adicionando uma nova linha ou modificando uma linha existente.</span><span class="sxs-lookup"><span data-stu-id="42ffa-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="42ffa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42ffa-106">Parameters</span></span>

 <span data-ttu-id="42ffa-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="42ffa-107">_cValues_</span></span>
  
> <span data-ttu-id="42ffa-108">no A contagem de propriedades a serem incluídas na linha da tabela de status novo ou modificado.</span><span class="sxs-lookup"><span data-stu-id="42ffa-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="42ffa-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="42ffa-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="42ffa-110">no Um ponteiro para uma matriz de valores de propriedade que descrevem as propriedades a serem incluídas como colunas na linha da tabela de status novo ou modificado.</span><span class="sxs-lookup"><span data-stu-id="42ffa-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="42ffa-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="42ffa-111">_ulFlags_</span></span>
  
> <span data-ttu-id="42ffa-112">no Uma bitmask de sinalizadores que controlam como as informações que definem a linha da tabela de status são processadas.</span><span class="sxs-lookup"><span data-stu-id="42ffa-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="42ffa-113">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="42ffa-113">The following flag can be set:</span></span>
    
<span data-ttu-id="42ffa-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="42ffa-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="42ffa-115">Direciona o MAPI a mesclar as propriedades incluídas na matriz apontadas por _lpColumnVals_ com uma linha de tabela de status existente, e não em uma nova linha.</span><span class="sxs-lookup"><span data-stu-id="42ffa-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="42ffa-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="42ffa-116">Return value</span></span>

<span data-ttu-id="42ffa-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="42ffa-117">S_OK</span></span> 
  
> <span data-ttu-id="42ffa-118">A tabela de status foi atualizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="42ffa-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42ffa-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="42ffa-119">Remarks</span></span>

<span data-ttu-id="42ffa-120">O método **IMAPISupport:: ModifyStatusRow** é implementado para todos os objetos de suporte do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="42ffa-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="42ffa-121">Os provedores de serviços chamam **ModifyStatusRow** no momento do logon para adicionar uma linha à tabela de status e em outros momentos durante a sessão para atualizar a linha.</span><span class="sxs-lookup"><span data-stu-id="42ffa-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="42ffa-122">O **ModifyStatusRow** fornece MAPI com as informações necessárias para criar a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="42ffa-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="42ffa-123">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="42ffa-123">Notes to callers</span></span>

<span data-ttu-id="42ffa-124">Defina o sinalizador STATUSROW_UPDATE quando você chamar **ModifyStatusRow** para fazer alterações nas propriedades da linha da tabela de status existente.</span><span class="sxs-lookup"><span data-stu-id="42ffa-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="42ffa-125">Isso informa ao MAPI que apenas as colunas que estão sendo alteradas são passadas no parâmetro _lpColumnVals_ .</span><span class="sxs-lookup"><span data-stu-id="42ffa-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="42ffa-126">Os clientes podem usar as informações na tabela de status para acessar o objeto status.</span><span class="sxs-lookup"><span data-stu-id="42ffa-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="42ffa-127">Para obter uma lista completa das colunas que devem ser incluídas na linha da tabela de status, consulte [tabelas de status](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="42ffa-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="42ffa-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="42ffa-128">See also</span></span>



[<span data-ttu-id="42ffa-129">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="42ffa-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

