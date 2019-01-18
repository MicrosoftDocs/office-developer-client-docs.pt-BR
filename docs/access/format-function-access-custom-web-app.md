---
title: Função Format (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Retorna um valor formatado de acordo com um padrão específico.
localization_priority: Priority
ms.openlocfilehash: 5331df30f276a7edd0571e9bf24c759d57ec6a54
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710388"
---
# <a name="format-function-access-custom-web-app"></a><span data-ttu-id="1d75c-103">Função Format (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="1d75c-103">Format Function (Access custom web app)</span></span>

<span data-ttu-id="1d75c-104">Retorna um valor formatado de acordo com um padrão específico.</span><span class="sxs-lookup"><span data-stu-id="1d75c-104">Returns a value formatted according to a specified pattern.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1d75c-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="1d75c-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="1d75c-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="1d75c-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1d75c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d75c-107">Syntax</span></span>

 <span data-ttu-id="1d75c-108">**Formato** (*Expressão*, *Formato*)</span><span class="sxs-lookup"><span data-stu-id="1d75c-108">**Format** (*Expression*, *Format*)</span></span> 
  
<span data-ttu-id="1d75c-109">A função **Formato** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="1d75c-109">The **Format** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="1d75c-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="1d75c-110">**Argument name**</span></span>|<span data-ttu-id="1d75c-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1d75c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1d75c-112">*Expressão*.</span><span class="sxs-lookup"><span data-stu-id="1d75c-112">*Expression*</span></span>  <br/> |<span data-ttu-id="1d75c-113">Expressão de um tipo de dados com suporte para formatar.</span><span class="sxs-lookup"><span data-stu-id="1d75c-113">Expression of a supported data type to format.</span></span>  <br/> |
| <span data-ttu-id="1d75c-114">*Formato*</span><span class="sxs-lookup"><span data-stu-id="1d75c-114">*Format*</span></span>  <br/> | <span data-ttu-id="1d75c-115">Um padrão de formatação.</span><span class="sxs-lookup"><span data-stu-id="1d75c-115">A format pattern.</span></span> <span data-ttu-id="1d75c-116">O argumento de formato deve conter uma cadeia de caracteres de formato válida, como uma cadeia de caracteres de formato padrão (por exemplo, "C" ou "D") ou como um padrão de caracteres personalizados para datas e valores numéricos (por exemplo, "MMMM dd, (dddd) aaaa").</span><span class="sxs-lookup"><span data-stu-id="1d75c-116">The format argument must contain a valid format string, either as a standard format string (for example, "C" or "D"), or as a pattern of custom characters for dates and numeric values (for example, "MMMM dd, yyyy (dddd)").</span></span> <span data-ttu-id="1d75c-117">Para saber mais, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="1d75c-117">For more information, see Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d75c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d75c-118">Remarks</span></span>

<span data-ttu-id="1d75c-119">Para o parâmetro *Formato*, você pode passar cadeias de caracteres que correspondam a qualquer um dos seguintes padrões:</span><span class="sxs-lookup"><span data-stu-id="1d75c-119">For the  *Format*  parameter, you can pass strings that match any of the following patterns:</span></span> 
  
- [<span data-ttu-id="1d75c-120">Cadeias de caracteres de formato numérico padrão</span><span class="sxs-lookup"><span data-stu-id="1d75c-120">Standard Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="1d75c-121">Cadeias de caracteres de formato numérico personalizado</span><span class="sxs-lookup"><span data-stu-id="1d75c-121">Custom Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="1d75c-122">Cadeias de caracteres padrão de formato de data e hora</span><span class="sxs-lookup"><span data-stu-id="1d75c-122">Standard Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="1d75c-123">Cadeias de caracteres de formato de data e hora</span><span class="sxs-lookup"><span data-stu-id="1d75c-123">Custom Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)
    
<span data-ttu-id="1d75c-124">Não é possível usar a função **Format** nas seguintes áreas de aplicativos Web do Access 2013:</span><span class="sxs-lookup"><span data-stu-id="1d75c-124">You cannot use the **Format** function in the following areas of Access 2013 web apps:</span></span> 
  
- <span data-ttu-id="1d75c-125">Colunas calculadas ao nível da tabela</span><span class="sxs-lookup"><span data-stu-id="1d75c-125">Calculated columns at the table level</span></span>
    
- <span data-ttu-id="1d75c-126">Macros de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1d75c-126">UI macros</span></span>
    
- <span data-ttu-id="1d75c-127">Expressões nos modos de exibição (por exemplo, em formulários)</span><span class="sxs-lookup"><span data-stu-id="1d75c-127">Expressions in views (for example, in forms)</span></span>
    

