---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a187245b2594282bc9908b3075852440f418af2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766498"
---
# <a name="dtpage"></a><span data-ttu-id="66107-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="66107-103">DTPAGE</span></span>

  
  
<span data-ttu-id="66107-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="66107-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="66107-105">Descreve a caixa de diálogo que é construída a partir de uma tabela de exibição pela função [BuildDisplayTable](builddisplaytable.md) .</span><span class="sxs-lookup"><span data-stu-id="66107-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66107-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="66107-106">Header file:</span></span>  <br/> |<span data-ttu-id="66107-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66107-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a><span data-ttu-id="66107-108">Members</span><span class="sxs-lookup"><span data-stu-id="66107-108">Members</span></span>

 <span data-ttu-id="66107-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="66107-109">**cctl**</span></span>
  
> <span data-ttu-id="66107-110">Contagem de controles apontado pelo membro **lpctl** .</span><span class="sxs-lookup"><span data-stu-id="66107-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="66107-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="66107-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="66107-112">Ponteiro para o nome ou número inteiro identificador para o recurso de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="66107-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="66107-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="66107-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="66107-114">Ponteiro para a cadeia de caracteres que aparece na seção **[Help File Mappings]** em MAPISVC.</span><span class="sxs-lookup"><span data-stu-id="66107-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="66107-115">Como **lpszComponent** está em uma união com o membro **ulItemID** , somente um desses membros tem dados válidos.</span><span class="sxs-lookup"><span data-stu-id="66107-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="66107-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="66107-116">**ulItemID**</span></span>
  
> <span data-ttu-id="66107-117">Identificador de recurso inteiro com um valor menor ou igual a 65535 do qual o nome do arquivo de Ajuda pode ser lidas.</span><span class="sxs-lookup"><span data-stu-id="66107-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="66107-118">Como **ulItemID** está em uma união com o membro **lpszComponent** , somente um desses membros tem dados válidos.</span><span class="sxs-lookup"><span data-stu-id="66107-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="66107-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="66107-119">**lpctl**</span></span>
  
> <span data-ttu-id="66107-120">Ponteiro para uma matriz de estruturas [DTCTL](dtctl.md) , um para cada controle na página.</span><span class="sxs-lookup"><span data-stu-id="66107-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="66107-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="66107-121">Remarks</span></span>

<span data-ttu-id="66107-122">Para identificar o arquivo de ajuda para a página com guias, defina o membro **lpszComponent** para uma cadeia de caracteres codificada ou o membro **ulItemID** como um identificador de recurso inteiro.</span><span class="sxs-lookup"><span data-stu-id="66107-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="66107-123">Cada entrada na seção **[Help File Mappings]** em MAPISVC. INF consiste em uma cadeia de componente, não mais de 30 caracteres, no lado esquerdo e um caminho de arquivo de ajuda à direita.</span><span class="sxs-lookup"><span data-stu-id="66107-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="66107-124">**UlItemID** e o **lpszResourceName** são encontrados no parâmetro _hInstance_ do **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="66107-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="66107-125">Para obter mais informações, consulte [MAPISVC. Seção do INF [mapeamentos do arquivo de ajuda]](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="66107-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="66107-126">Embora **BuildDisplayTable** usa essa estrutura para criar a tabela de exibição de recursos de controle, a estrutura **DTPAGE** nunca será exibida na tabela a exibição em si.</span><span class="sxs-lookup"><span data-stu-id="66107-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="66107-127">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="66107-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="66107-128">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="66107-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66107-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="66107-129">See also</span></span>



[<span data-ttu-id="66107-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="66107-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="66107-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="66107-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="66107-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="66107-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="66107-133">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="66107-133">MAPI Structures</span></span>](mapi-structures.md)

