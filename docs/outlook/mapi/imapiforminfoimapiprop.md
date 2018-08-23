---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2b2abf4440ee2d81a8e95dcdb5fde2daeaa6e6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575907"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="48a21-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="48a21-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="48a21-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48a21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48a21-105">Aplicativos cliente de fornece acesso às propriedades específicas para a definição do formulário.</span><span class="sxs-lookup"><span data-stu-id="48a21-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="48a21-106">Mantendo as informações do formulário em um objeto separado, o provedor de bibliotecas de formulário pode descrever um formulário para um cliente sem ativando o formulário.</span><span class="sxs-lookup"><span data-stu-id="48a21-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48a21-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="48a21-107">Header file:</span></span>  <br/> |<span data-ttu-id="48a21-108">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="48a21-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="48a21-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="48a21-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="48a21-110">Objetos de informações de formulário</span><span class="sxs-lookup"><span data-stu-id="48a21-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="48a21-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="48a21-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="48a21-112">Provedores de biblioteca de formulário</span><span class="sxs-lookup"><span data-stu-id="48a21-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="48a21-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="48a21-113">Called by:</span></span>  <br/> |<span data-ttu-id="48a21-114">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="48a21-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="48a21-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="48a21-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="48a21-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="48a21-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="48a21-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="48a21-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="48a21-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="48a21-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="48a21-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="48a21-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="48a21-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="48a21-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="48a21-121">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="48a21-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="48a21-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="48a21-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="48a21-123">Retorna um ponteiro para o conjunto completo de propriedades que usa um formulário.</span><span class="sxs-lookup"><span data-stu-id="48a21-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="48a21-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="48a21-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="48a21-125">Retorna um ponteiro para o conjunto completo de verbos que usa um formulário.</span><span class="sxs-lookup"><span data-stu-id="48a21-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="48a21-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="48a21-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="48a21-127">Um ícone de uma propriedade de ícone de um formulário se baseia.</span><span class="sxs-lookup"><span data-stu-id="48a21-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="48a21-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="48a21-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="48a21-129">Salva uma descrição de um determinado formulário em um arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="48a21-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="48a21-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="48a21-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="48a21-131">Retorna um ponteiro para o contêiner de formulário na qual um determinado formulário está instalado.</span><span class="sxs-lookup"><span data-stu-id="48a21-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48a21-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="48a21-132">Remarks</span></span>

<span data-ttu-id="48a21-133">Ao contrário da maioria das interfaces definidas no arquivo de cabeçalho MapiForm.h, **IMAPIFormInfo** herda da interface [IMAPIProp](imapipropiunknown.md) , pois ele exporta a maioria das informações do formulário por meio de chamadas para o método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="48a21-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48a21-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="48a21-134">See also</span></span>



[<span data-ttu-id="48a21-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="48a21-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

