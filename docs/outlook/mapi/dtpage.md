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
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408219"
---
# <a name="dtpage"></a><span data-ttu-id="883b6-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="883b6-103">DTPAGE</span></span>

  
  
<span data-ttu-id="883b6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="883b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="883b6-105">Descreve a caixa de diálogo criada a partir de uma tabela de exibição pela [função BuildDisplayTable.](builddisplaytable.md)</span><span class="sxs-lookup"><span data-stu-id="883b6-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="883b6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="883b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="883b6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="883b6-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="883b6-108">Members</span><span class="sxs-lookup"><span data-stu-id="883b6-108">Members</span></span>

 <span data-ttu-id="883b6-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="883b6-109">**cctl**</span></span>
  
> <span data-ttu-id="883b6-110">Contagem de controles apontados pelo **membro lpctl.**</span><span class="sxs-lookup"><span data-stu-id="883b6-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="883b6-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="883b6-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="883b6-112">Ponteiro para o nome ou identificador inteiro do recurso da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="883b6-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="883b6-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="883b6-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="883b6-114">Ponteiro para a cadeia de caracteres que aparece na seção **[Mapeamentos** de Arquivo de Ajuda] em MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="883b6-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="883b6-115">Como **lpszComponent** está em uma união com o membro **ulItemID,** apenas um desses membros tem dados válidos.</span><span class="sxs-lookup"><span data-stu-id="883b6-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="883b6-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="883b6-116">**ulItemID**</span></span>
  
> <span data-ttu-id="883b6-117">Identificador de recurso integer com um valor menor ou igual a 65535 a partir do qual o nome do arquivo de Ajuda pode ser lido.</span><span class="sxs-lookup"><span data-stu-id="883b6-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="883b6-118">Como **ulItemID** está em uma união com o membro **lpszComponent,** apenas um desses membros tem dados válidos.</span><span class="sxs-lookup"><span data-stu-id="883b6-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="883b6-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="883b6-119">**lpctl**</span></span>
  
> <span data-ttu-id="883b6-120">Ponteiro para uma matriz de [estruturas DTCTL,](dtctl.md) um para cada controle na página.</span><span class="sxs-lookup"><span data-stu-id="883b6-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="883b6-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="883b6-121">Remarks</span></span>

<span data-ttu-id="883b6-122">Para identificar o arquivo de Ajuda para a página com guias, de definir o membro **lpszComponent** como uma cadeia de caracteres embutida em código ou o membro **ulItemID** como um identificador de recurso inteiro.</span><span class="sxs-lookup"><span data-stu-id="883b6-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="883b6-123">Cada entrada na seção **[Mapeamentos de Arquivo de Ajuda]** no MAPISVC. INF consiste em uma cadeia de caracteres de componente, não mais do que 30 caracteres, no lado esquerdo e um caminho de arquivo de Ajuda à direita.</span><span class="sxs-lookup"><span data-stu-id="883b6-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="883b6-124">Tanto **ulItemID** quanto **lpszResourceName são** encontrados no  _parâmetro hInstance_ de **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="883b6-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="883b6-125">Para obter mais informações, consulte [MAPISVC. Seção INF [Mapeamentos de Arquivos de Ajuda]](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="883b6-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="883b6-126">Embora **BuildDisplayTable** use essa estrutura para criar a tabela de exibição a partir de recursos de controle, a estrutura **DTPAGE** nunca aparece na própria tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="883b6-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="883b6-127">Para uma visão geral das tabelas de exibição, consulte [Tabelas de Exibição.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="883b6-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="883b6-128">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="883b6-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="883b6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="883b6-129">See also</span></span>



[<span data-ttu-id="883b6-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="883b6-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="883b6-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="883b6-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="883b6-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="883b6-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="883b6-133">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="883b6-133">MAPI Structures</span></span>](mapi-structures.md)

