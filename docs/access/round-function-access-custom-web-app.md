---
title: Função Round (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Retorna um valor numérico, arredondado ou truncado, para o comprimento ou precisão especificado.
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307956"
---
# <a name="round-function-access-custom-web-app"></a><span data-ttu-id="43dfd-103">Função Round (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="43dfd-103">Round Function (Access custom web app)</span></span>

<span data-ttu-id="43dfd-104">Retorna um valor numérico, arredondado ou truncado, para o comprimento ou precisão especificado.</span><span class="sxs-lookup"><span data-stu-id="43dfd-104">Returns a numeric value, either rounded or truncated, to the specified length or precision.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="43dfd-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="43dfd-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="43dfd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43dfd-107">Syntax</span></span>

 <span data-ttu-id="43dfd-108">**Round** (*Número*, *Precisão*, [*TruncateInsteadOfRound*])</span><span class="sxs-lookup"><span data-stu-id="43dfd-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span></span> 
  
<span data-ttu-id="43dfd-109">A função **Round** contém os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="43dfd-109">The **Round** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="43dfd-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="43dfd-110">**Argument name**</span></span>|<span data-ttu-id="43dfd-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="43dfd-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="43dfd-112">*Número*</span><span class="sxs-lookup"><span data-stu-id="43dfd-112">*Number*</span></span>  <br/> |<span data-ttu-id="43dfd-113">Uma expressão numérica</span><span class="sxs-lookup"><span data-stu-id="43dfd-113">A numeric expression.</span></span>  <br/> |
| <span data-ttu-id="43dfd-114">*Precisão*</span><span class="sxs-lookup"><span data-stu-id="43dfd-114">*Precision*</span></span>  <br/> |<span data-ttu-id="43dfd-p102">A precisão com a qual o  *Número*  deve ser arredondado.  *Precisão*  deve ser uma expressão numérica. Quando  *Precisão*  for um número positivo,  *Número*  será arredondado para o número de posições decimais especificados por comprimento. Quando  *Precisão*  for um número negativo,  *Número*  será arredondado no lado esquerdo da vírgula decimal, como especificado por comprimento.  </span><span class="sxs-lookup"><span data-stu-id="43dfd-p102">The precision to which  *Number*  is to be rounded.  *Precision*  must be a numeric expression. When  *Precision*  is a positive number,  *Number*  is rounded to the number of decimal positions specified by length. When  *Precision*  is a negative number,  *Number*  is rounded on the left side of the decimal point, as specified by length.  </span></span><br/> |
| <span data-ttu-id="43dfd-119">*TruncateInsteadOfRound*</span><span class="sxs-lookup"><span data-stu-id="43dfd-119">*TruncateInsteadOfRound*</span></span>  <br/> |<span data-ttu-id="43dfd-p103">O tipo de operação a ser executada. Quando omitido ou definido como 0,  *Número*  será arredondado. Quando um valor diferente de 0 for especificado,  *Número*  será truncado. O valor padrão é 0.  </span><span class="sxs-lookup"><span data-stu-id="43dfd-p103">The type of operation to perform. When omitted or set to 0,  *Number*  is rounded. When a value other than 0 is specified,  *Number*  is truncated. The default value is 0.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="43dfd-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="43dfd-124">Remarks</span></span>

 <span data-ttu-id="43dfd-p104">**Round** sempre retorna um valor. Se o comprimento for negativo e maior do que o número de dígitos anteriores à vírgula decimal, **Round** retornará 0.</span><span class="sxs-lookup"><span data-stu-id="43dfd-p104">**Round** always returns a value. If length is negative and larger than the number of digits before the decimal point, **Round** returns 0.</span></span> 
  

