---
title: '[Não] é NULL (aplicativo da web personalizado do Access)'
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Determina se a expressão especificada é NULL.
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765075"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="e68b4-103">[Não] é NULL (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="e68b4-103">IS [NOT] NULL (Access custom web app)</span></span>

<span data-ttu-id="e68b4-104">Determina se a expressão especificada é NULL.</span><span class="sxs-lookup"><span data-stu-id="e68b4-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e68b4-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="e68b4-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e68b4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e68b4-107">Syntax</span></span>

 <span data-ttu-id="e68b4-108">*expressão* **Encontra** [ *Não* ] **Nulo**</span><span class="sxs-lookup"><span data-stu-id="e68b4-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="e68b4-109">O **IS [NOT] NULL** predicado contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e68b4-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e68b4-110">*expressão*</span><span class="sxs-lookup"><span data-stu-id="e68b4-110">*expression*</span></span>  <br/> |<span data-ttu-id="e68b4-111">Qualquer expressão válida.</span><span class="sxs-lookup"><span data-stu-id="e68b4-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="e68b4-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="e68b4-112">*NOT*</span></span>  <br/> |<span data-ttu-id="e68b4-113">Especifica que o resultado booleano ser negadas.</span><span class="sxs-lookup"><span data-stu-id="e68b4-113">Specifies that the Boolean result be negated.</span></span> <span data-ttu-id="e68b4-114">O predicado reverte seus valores de retorno, retornando TRUE se o valor não for NULL e FALSE se o valor é nulo.</span><span class="sxs-lookup"><span data-stu-id="e68b4-114">The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e68b4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e68b4-115">Remarks</span></span>

<span data-ttu-id="e68b4-116">Se o valor da *expressão* for NULL, é nulo retorna TRUE; Caso contrário, ele retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="e68b4-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="e68b4-117">Se o valor da expressão for NULL, não é NULL retorna FALSE; Caso contrário, ele retornará TRUE.</span><span class="sxs-lookup"><span data-stu-id="e68b4-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

