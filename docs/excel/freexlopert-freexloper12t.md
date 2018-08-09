---
title: FreeXLOperT/FreeXLOper12T
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FreeXLOper12T
- FreeXLOperT
keywords:
- função freexlopert [excel 2007], função FreeXLOper12T [Excel 2007]
localization_priority: Normal
ms.assetid: 8fb3fdfd-8a43-4c50-82ff-e701fed3d83f
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b7411bc51770dadc7c2d4a5c2c65d2d546f6025f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765377"
---
# <a name="freexlopertfreexloper12t"></a><span data-ttu-id="2b147-104">FreeXLOperT/FreeXLOper12T</span><span class="sxs-lookup"><span data-stu-id="2b147-104">FreeXLOperT/FreeXLOper12T</span></span>

 <span data-ttu-id="2b147-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2b147-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2b147-106">Função Framework que libera a memória associada a um **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="2b147-106">Framework function that frees memory associated with an **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="2b147-107">A função pressupõe que a memória foi alocada com chamadas para malloc dentro da DLL.</span><span class="sxs-lookup"><span data-stu-id="2b147-107">The function assumes that the memory was allocated with calls to malloc within the DLL.</span></span> <span data-ttu-id="2b147-108">Se a memória foi alocada pelo Microsoft Excel ou de alguma outra forma ou por algum outro processo, essa função não deve ser usada para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="2b147-108">If the memory was allocated by Microsoft Excel or in some other way or by some other process, this function should not be used to free the memory.</span></span> <span data-ttu-id="2b147-109">Use [xlFree](xlfree.md) para liberar memória alocada pelo Excel para **XLOPER**/ **XLOPER12**s.</span><span class="sxs-lookup"><span data-stu-id="2b147-109">Use [xlFree](xlfree.md) to free memory allocated by Excel for **XLOPER**/ **XLOPER12**s.</span></span> 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="2b147-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b147-110">Parameters</span></span>

 <span data-ttu-id="2b147-111">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="2b147-111">_pxloper_ (**LPXLOPER**)</span></span>
  
 <span data-ttu-id="2b147-112">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="2b147-112">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="2b147-113">Ponteiro para **XLOPER**/ **XLOPER12** serem liberados.</span><span class="sxs-lookup"><span data-stu-id="2b147-113">Pointer to the **XLOPER**/ **XLOPER12** to be freed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2b147-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2b147-114">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
void FreeXLOper12T(LPXLOPER12 pxloper12)
{
   DWORD xltype;
   int cxloper12;
   LPXLOPER12 pxloper12Free;
   xltype = pxloper12->xltype;
   switch (xltype)
   {
   case xltypeStr:
      if (pxloper12->val.str != NULL)
         free(pxloper12->val.str);
      break;
   case xltypeRef:
      if (pxloper12->val.mref.lpmref != NULL)
         free(pxloper12->val.mref.lpmref);
      break;
   case xltypeMulti:
      cxloper12 = pxloper12->val.array.rows * pxloper12->val.array.columns;
      if (pxloper12->val.array.lparray)
      {
         pxloper12Free = pxloper12->val.array.lparray;
         while (cxloper12 > 0)
         {
            FreeXLOper12T(pxloper12Free);
            pxloper12Free++;
            cxloper12--;
         }
         free(pxloper12->val.array.lparray);
      }
      break;
   case xltypeBigData:
      if (pxloper12->val.bigdata.h.lpbData != NULL)
         free(pxloper12->val.bigdata.h.lpbData);
      break;
   }
}
```

## <a name="see-also"></a><span data-ttu-id="2b147-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b147-115">See also</span></span>



[<span data-ttu-id="2b147-116">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="2b147-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

