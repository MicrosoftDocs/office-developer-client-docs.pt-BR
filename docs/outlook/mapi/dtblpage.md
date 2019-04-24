---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340114"
---
# <a name="dtblpage"></a><span data-ttu-id="7c242-103">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="7c242-103">DTBLPAGE</span></span>

  
  
<span data-ttu-id="7c242-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c242-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c242-105">Descreve uma página com guias que será usada em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="7c242-105">Describes a tabbed page that will be used in a dialog box that is built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c242-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7c242-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c242-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7c242-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7c242-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="7c242-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="7c242-109">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="7c242-109">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a><span data-ttu-id="7c242-110">Members</span><span class="sxs-lookup"><span data-stu-id="7c242-110">Members</span></span>

 <span data-ttu-id="7c242-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="7c242-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="7c242-112">Posição na memória do rótulo de cadeia de caracteres para a guia de página.</span><span class="sxs-lookup"><span data-stu-id="7c242-112">Position in memory of the character string label for the page tab.</span></span>
    
 <span data-ttu-id="7c242-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="7c242-113">**ulFlags**</span></span>
  
> <span data-ttu-id="7c242-114">Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="7c242-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="7c242-115">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="7c242-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="7c242-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7c242-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7c242-117">O rótulo está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7c242-117">The label is in Unicode format.</span></span> <span data-ttu-id="7c242-118">Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo estará no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="7c242-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="7c242-119">**ulbLpszComponent**</span><span class="sxs-lookup"><span data-stu-id="7c242-119">**ulbLpszComponent**</span></span>
  
> <span data-ttu-id="7c242-120">Posição na memória de uma cadeia de caracteres que identifica a seção **[help file Mappings]** no MAPISVC. Arquivo de configuração INF ou 0.</span><span class="sxs-lookup"><span data-stu-id="7c242-120">Position in memory of a character string identifying the **[Help File Mappings]** section in the MAPISVC.INF configuration file or 0.</span></span> <span data-ttu-id="7c242-121">O nome do arquivo que aparece no MAPISVC. A seção INF pode ser usada por um usuário para acessar a ajuda estendida para a página com guias clicando no botão **ajuda** na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7c242-121">The file name appearing in the MAPISVC.INF section can be used by a user to access extended Help for the tabbed page by clicking the **Help** button in the dialog box.</span></span> <span data-ttu-id="7c242-122">Para obter mais informações sobre as entradas em MAPISVC. INF, consulte [formato de arquivo de MAPISVC. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="7c242-122">For more information about the entries in MAPISVC.INF, see [File Format of MAPISVC.INF](file-format-of-mapisvc-inf.md).</span></span>
    
 <span data-ttu-id="7c242-123">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="7c242-123">**ulContext**</span></span>
  
> <span data-ttu-id="7c242-124">Um identificador exclusivo para a página com guias na cadeia de caracteres definida pelo membro **ulbLpszComponent** .</span><span class="sxs-lookup"><span data-stu-id="7c242-124">A unique identifier for the tabbed page in the string defined by the **ulbLpszComponent** member.</span></span> <span data-ttu-id="7c242-125">O membro **ulbLpszComponent** e o membro **ulContext** devem ser diferentes de zero para que o botão **ajuda** funcione.</span><span class="sxs-lookup"><span data-stu-id="7c242-125">The **ulbLpszComponent** member and the **ulContext** member must both be nonzero for the **Help** button to work.</span></span> <span data-ttu-id="7c242-126">Se esse identificador for zero e a cadeia de caracteres do componente for nula, não haverá ajuda associada à página.</span><span class="sxs-lookup"><span data-stu-id="7c242-126">If this identifier is zero and the component string is NULL, there is no Help associated with the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7c242-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c242-127">Remarks</span></span>

<span data-ttu-id="7c242-128">Uma estrutura **DTBLPAGE** descreve uma página com guias um controle que é usado para separar várias caixas de diálogo relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7c242-128">A **DTBLPAGE** structure describes a tabbed page a control that is used to separate several related dialog boxes.</span></span> <span data-ttu-id="7c242-129">Normalmente, essas caixas de diálogo são folhas de propriedades para exibir opções de configuração, mensagem ou destinatário.</span><span class="sxs-lookup"><span data-stu-id="7c242-129">Typically, these dialog boxes are property sheets for displaying configuration, message, or recipient options.</span></span> <span data-ttu-id="7c242-130">Ao clicar na guia, o usuário pode alternar de uma planilha para outra.</span><span class="sxs-lookup"><span data-stu-id="7c242-130">By clicking the tab, the user can switch from one sheet to another.</span></span> 
  
<span data-ttu-id="7c242-131">A cadeia de caracteres do componente e o identificador de contexto fornecem informações sobre se a ajuda estendida está disponível para a página com guias.</span><span class="sxs-lookup"><span data-stu-id="7c242-131">The component string and context identifier provide information about whether extended Help is available for the tabbed page.</span></span> <span data-ttu-id="7c242-132">Se a ajuda estendida estiver disponível, a cadeia de caracteres do componente e o identificador de contexto fornecerão informações sobre como acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="7c242-132">If extended Help is available, the component string and context identifier will provide information about how to access it.</span></span> <span data-ttu-id="7c242-133">A cadeia de caracteres do componente mapeia para o arquivo de ajuda; o identificador de contexto é mapeado para o tópico de ajuda inicial.</span><span class="sxs-lookup"><span data-stu-id="7c242-133">The component string maps to the Help file; the context identifier maps to the initial Help topic.</span></span> <span data-ttu-id="7c242-134">Se o identificador de contexto for zero e a cadeia de caracteres do componente for nula, a ajuda estendida não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="7c242-134">If the context identifier is zero and the component string is NULL, extended Help is not available.</span></span>
  
<span data-ttu-id="7c242-135">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7c242-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="7c242-136">Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="7c242-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c242-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c242-137">See also</span></span>



[<span data-ttu-id="7c242-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="7c242-138">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="7c242-139">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="7c242-139">MAPI Structures</span></span>](mapi-structures.md)

