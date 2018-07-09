---
title: Função Format (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Retorna um valor formatado de acordo com um padrão especificado.
ms.openlocfilehash: 974b56ab8e6bc3f97c1931ba67ca9cd08c3511c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765091"
---
# <a name="format-function-access-custom-web-app"></a><span data-ttu-id="13af3-103">Função Format (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="13af3-103">Format Function (Access custom web app)</span></span>

<span data-ttu-id="13af3-104">Retorna um valor formatado de acordo com um padrão especificado.</span><span class="sxs-lookup"><span data-stu-id="13af3-104">Returns a value formatted according to a specified pattern.</span></span>
  
> [!NOTE]
> <span data-ttu-id="13af3-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="13af3-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="13af3-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="13af3-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="13af3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13af3-107">Syntax</span></span>

 <span data-ttu-id="13af3-108">**Formato** (*Expressão*, *formato*)</span><span class="sxs-lookup"><span data-stu-id="13af3-108">**Format** (*Expression*, *Format*)</span></span> 
  
<span data-ttu-id="13af3-109">A função **Format** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="13af3-109">The **Format** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="13af3-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="13af3-110">**Argument name**</span></span>|<span data-ttu-id="13af3-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="13af3-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="13af3-112">*Expressão*</span><span class="sxs-lookup"><span data-stu-id="13af3-112">*Expression*</span></span>  <br/> |<span data-ttu-id="13af3-113">Expressão de um tipo de dados com suporte para formatar.</span><span class="sxs-lookup"><span data-stu-id="13af3-113">Expression of a supported data type to format.</span></span>  <br/> |
| <span data-ttu-id="13af3-114">*Format*</span><span class="sxs-lookup"><span data-stu-id="13af3-114">*Format*</span></span>  <br/> | <span data-ttu-id="13af3-115">Um formato padrão.</span><span class="sxs-lookup"><span data-stu-id="13af3-115">A format pattern.</span></span> <span data-ttu-id="13af3-116">O argumento format deve conter uma cadeia de caracteres de formato válido, como uma cadeia de caracteres de formato padrão (por exemplo, "C" ou "D"), ou como um padrão de caracteres personalizados para datas e os valores numéricos (por exemplo, "MMMM dd, yyyy (dddd)").</span><span class="sxs-lookup"><span data-stu-id="13af3-116">The format argument must contain a valid format string, either as a standard format string (for example, "C" or "D"), or as a pattern of custom characters for dates and numeric values (for example, "MMMM dd, yyyy (dddd)").</span></span> <span data-ttu-id="13af3-117">Para obter mais informações, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="13af3-117">For more information, see Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13af3-118">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="13af3-118">Remarks</span></span>

<span data-ttu-id="13af3-119">Para o parâmetro *Format* , você pode passar cadeias de caracteres que correspondam a qualquer um dos seguintes padrões:</span><span class="sxs-lookup"><span data-stu-id="13af3-119">For the  *Format*  parameter, you can pass strings that match any of the following patterns:</span></span> 
  
- [<span data-ttu-id="13af3-120">Cadeias de caracteres de formato numérico padrão</span><span class="sxs-lookup"><span data-stu-id="13af3-120">Standard Numeric Format Strings</span></span>](http://msdn.microsoft.com/pt-br/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="13af3-121">Cadeias de caracteres de formato numérico personalizado</span><span class="sxs-lookup"><span data-stu-id="13af3-121">Custom Numeric Format Strings</span></span>](http://msdn.microsoft.com/pt-br/library/0c899ak8%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="13af3-122">As cadeias de caracteres de formato padrão de data e hora</span><span class="sxs-lookup"><span data-stu-id="13af3-122">Standard Date and Time Format Strings</span></span>](http://msdn.microsoft.com/pt-br/library/az4se3k1%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="13af3-123">As cadeias de caracteres de formato de data e hora personalizado</span><span class="sxs-lookup"><span data-stu-id="13af3-123">Custom Date and Time Format Strings</span></span>](http://msdn.microsoft.com/pt-br/library/8kb3ddd4%28v=vs.110%29.aspx)
    
<span data-ttu-id="13af3-124">Você não pode usar a função **Format** nas seguintes áreas do Access 2013 web apps:</span><span class="sxs-lookup"><span data-stu-id="13af3-124">You cannot use the **Format** function in the following areas of Access 2013 web apps:</span></span> 
  
- <span data-ttu-id="13af3-125">Colunas calculadas no nível de tabela</span><span class="sxs-lookup"><span data-stu-id="13af3-125">Calculated columns at the table level</span></span>
    
- <span data-ttu-id="13af3-126">Macros de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="13af3-126">UI macros</span></span>
    
- <span data-ttu-id="13af3-127">Expressões em modos de exibição (por exemplo, em formulários)</span><span class="sxs-lookup"><span data-stu-id="13af3-127">Expressions in views (for example, in forms)</span></span>
    

