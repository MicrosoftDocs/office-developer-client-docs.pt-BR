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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a230e8b69a64646dffb23147345d5960fdd38581
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767034"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="47b9f-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="47b9f-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="47b9f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47b9f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47b9f-105">Um ícone de uma das propriedades ícone de um formulário se baseia.</span><span class="sxs-lookup"><span data-stu-id="47b9f-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="47b9f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="47b9f-106">Parameters</span></span>

 <span data-ttu-id="47b9f-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="47b9f-107">_nPropID_</span></span>
  
> <span data-ttu-id="47b9f-108">[in] Um identificador de propriedade para uma propriedade de ícone.</span><span class="sxs-lookup"><span data-stu-id="47b9f-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="47b9f-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="47b9f-109">_phicon_</span></span>
  
> <span data-ttu-id="47b9f-110">[out] Um ponteiro para o ícone retornado.</span><span class="sxs-lookup"><span data-stu-id="47b9f-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47b9f-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="47b9f-111">Return value</span></span>

<span data-ttu-id="47b9f-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="47b9f-112">S_OK</span></span> 
  
> <span data-ttu-id="47b9f-113">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="47b9f-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47b9f-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="47b9f-114">Remarks</span></span>

<span data-ttu-id="47b9f-115">Aplicativos cliente chamam o método de **IMAPIFormInfo::MakeIconFromBinary** para criar um ícone de uma das propriedades ícone de um formulário.</span><span class="sxs-lookup"><span data-stu-id="47b9f-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="47b9f-116">O parâmetro _nPropID_ , **MakeIconFromBinary** tira o identificador de propriedade de uma das propriedades ícone de um formulário.</span><span class="sxs-lookup"><span data-stu-id="47b9f-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="47b9f-117">Usando esse identificador de propriedade, ele cria um ícone que pode ser exibido nos modos de exibição de tabela que incluem colunas de propriedade de ícones.</span><span class="sxs-lookup"><span data-stu-id="47b9f-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47b9f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="47b9f-118">See also</span></span>



[<span data-ttu-id="47b9f-119">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="47b9f-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

