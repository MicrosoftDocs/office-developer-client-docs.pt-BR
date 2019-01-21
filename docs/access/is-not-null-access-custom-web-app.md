---
title: IS [NOT] NULL (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Determina se a expressão especificada é NULL.
localization_priority: Priority
ms.openlocfilehash: fe6a0fe4f182a1385304b783e7cfaaf515f732d4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699312"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="478e2-103">IS [NOT] NULL (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="478e2-103">IS [NOT] NULL (Access custom web app)</span></span>

<span data-ttu-id="478e2-104">Determina se a expressão especificada é NULL.</span><span class="sxs-lookup"><span data-stu-id="478e2-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="478e2-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-BR/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="478e2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-BR/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="478e2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="478e2-107">Syntax</span></span>

 <span data-ttu-id="478e2-108">*expression* **IS** [*NOT*] **NULL**</span><span class="sxs-lookup"><span data-stu-id="478e2-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="478e2-109">O predicado **IS [NOT] NULL** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="478e2-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="478e2-110">*expression*</span><span class="sxs-lookup"><span data-stu-id="478e2-110">*expression*</span></span>  <br/> |<span data-ttu-id="478e2-111">Qualquer expressão válida.</span><span class="sxs-lookup"><span data-stu-id="478e2-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="478e2-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="478e2-112">*NOT*</span></span>  <br/> |<span data-ttu-id="478e2-113">Especifica se o resultado booliano pode ser negado.</span><span class="sxs-lookup"><span data-stu-id="478e2-113">Specifies that the Boolean result be negated.</span></span> <span data-ttu-id="478e2-114">O predicado inverte os respectivos valores de retorno, retornando TRUE se o valor não for NULL e FALSE se o valor for NULL.</span><span class="sxs-lookup"><span data-stu-id="478e2-114">The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="478e2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="478e2-115">Remarks</span></span>

<span data-ttu-id="478e2-116">Se o valor de *expression* for NULL, então IS NULL retornará TRUE. Caso contrário, retornará FALSE.</span><span class="sxs-lookup"><span data-stu-id="478e2-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="478e2-117">Se o valor de expression for NULL, então IS NOT NULL retornará FALSE. Caso contrário, retornará TRUE.</span><span class="sxs-lookup"><span data-stu-id="478e2-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

