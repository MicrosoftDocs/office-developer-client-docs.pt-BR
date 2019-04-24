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
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321732"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="a01b7-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a01b7-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="a01b7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a01b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a01b7-105">Oferece aos aplicativos cliente acesso a propriedades que são específicas para a definição de formulários.</span><span class="sxs-lookup"><span data-stu-id="a01b7-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="a01b7-106">Ao manter as informações de formulário em um objeto separado, o provedor de biblioteca de formulários pode descrever um formulário para um cliente sem ativar o formulário.</span><span class="sxs-lookup"><span data-stu-id="a01b7-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a01b7-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a01b7-107">Header file:</span></span>  <br/> |<span data-ttu-id="a01b7-108">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="a01b7-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a01b7-109">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="a01b7-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a01b7-110">Objetos de informações de formulário</span><span class="sxs-lookup"><span data-stu-id="a01b7-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="a01b7-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a01b7-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a01b7-112">Provedores de biblioteca de formulários</span><span class="sxs-lookup"><span data-stu-id="a01b7-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="a01b7-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a01b7-113">Called by:</span></span>  <br/> |<span data-ttu-id="a01b7-114">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="a01b7-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="a01b7-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="a01b7-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a01b7-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="a01b7-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="a01b7-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="a01b7-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a01b7-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="a01b7-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="a01b7-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="a01b7-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="a01b7-120">Não-Transacted</span><span class="sxs-lookup"><span data-stu-id="a01b7-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a01b7-121">Vtable order</span><span class="sxs-lookup"><span data-stu-id="a01b7-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a01b7-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="a01b7-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="a01b7-123">Retorna um ponteiro para o conjunto completo de propriedades que um formulário usa.</span><span class="sxs-lookup"><span data-stu-id="a01b7-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="a01b7-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="a01b7-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="a01b7-125">Retorna um ponteiro para o conjunto completo de verbos que um formulário usa.</span><span class="sxs-lookup"><span data-stu-id="a01b7-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="a01b7-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="a01b7-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="a01b7-127">Cria um ícone a partir de uma Propriedade Icon de um formulário.</span><span class="sxs-lookup"><span data-stu-id="a01b7-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="a01b7-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="a01b7-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="a01b7-129">Salva uma descrição de um formulário específico em um arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="a01b7-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="a01b7-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="a01b7-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="a01b7-131">Retorna um ponteiro para o contêiner de formulários no qual um determinado formulário é instalado.</span><span class="sxs-lookup"><span data-stu-id="a01b7-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a01b7-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="a01b7-132">Remarks</span></span>

<span data-ttu-id="a01b7-133">Ao contrário da maioria das interfaces definidas no arquivo de cabeçalho MapiForm. h, o **IMAPIFormInfo** herda da interface [IMAPIProp](imapipropiunknown.md) , porque exporta a maioria das informações de formulário através de chamadas para o método [IMAPIProp::](imapiprop-getprops.md) GetProps.</span><span class="sxs-lookup"><span data-stu-id="a01b7-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a01b7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a01b7-134">See also</span></span>



[<span data-ttu-id="a01b7-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a01b7-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

