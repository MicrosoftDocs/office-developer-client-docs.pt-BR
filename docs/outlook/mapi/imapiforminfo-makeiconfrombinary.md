---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405111"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="5ca8c-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="5ca8c-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="5ca8c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ca8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ca8c-105">Cria um ícone a partir de uma das propriedades de ícone de um formulário.</span><span class="sxs-lookup"><span data-stu-id="5ca8c-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="5ca8c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ca8c-106">Parameters</span></span>

 <span data-ttu-id="5ca8c-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="5ca8c-107">_nPropID_</span></span>
  
> <span data-ttu-id="5ca8c-108">[in] Um identificador de propriedade para uma propriedade de ícone.</span><span class="sxs-lookup"><span data-stu-id="5ca8c-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="5ca8c-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="5ca8c-109">_phicon_</span></span>
  
> <span data-ttu-id="5ca8c-110">[out] Um ponteiro para o ícone retornado.</span><span class="sxs-lookup"><span data-stu-id="5ca8c-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ca8c-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5ca8c-111">Return value</span></span>

<span data-ttu-id="5ca8c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ca8c-112">S_OK</span></span> 
  
> <span data-ttu-id="5ca8c-113">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="5ca8c-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ca8c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ca8c-114">Remarks</span></span>

<span data-ttu-id="5ca8c-115">Os aplicativos cliente chamam o método **IMAPIFormInfo::MakeIconFromBinary** para criar um ícone a partir de uma das propriedades de ícone de um formulário.</span><span class="sxs-lookup"><span data-stu-id="5ca8c-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="5ca8c-116">No parâmetro  _nPropID,_ **MakeIconFromBinary** assume o identificador de propriedade de uma das propriedades de ícone de um formulário.</span><span class="sxs-lookup"><span data-stu-id="5ca8c-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="5ca8c-117">Usando esse identificador de propriedade, ele cria um ícone que pode ser exibido em exibições de tabela que incluem colunas de propriedade para ícones.</span><span class="sxs-lookup"><span data-stu-id="5ca8c-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ca8c-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ca8c-118">See also</span></span>



[<span data-ttu-id="5ca8c-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5ca8c-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

