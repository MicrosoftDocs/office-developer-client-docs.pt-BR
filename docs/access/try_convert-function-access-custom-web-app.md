---
title: Função Try_Convert (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Converte um valor em um tipo de dados especificada ou retorna Null se a conversão não é válida.
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765264"
---
# <a name="tryconvert-function-access-custom-web-app"></a><span data-ttu-id="a7511-103">Função Try_Convert (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="a7511-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="a7511-104">Converte um valor em um tipo de dados especificada ou retorna Null se a conversão não é válida.</span><span class="sxs-lookup"><span data-stu-id="a7511-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a7511-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="a7511-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a7511-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7511-107">Syntax</span></span>

 <span data-ttu-id="a7511-108">**Try_Convert** (*DataType*, *expressão*)</span><span class="sxs-lookup"><span data-stu-id="a7511-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="a7511-109">A função **Try_Convert** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a7511-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a7511-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="a7511-110">**Argument name**</span></span>|<span data-ttu-id="a7511-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a7511-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a7511-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="a7511-112">*DataType*</span></span>  <br/> |<span data-ttu-id="a7511-113">O tipo de dados no qual converter a *expressão* .</span><span class="sxs-lookup"><span data-stu-id="a7511-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="a7511-114">*Expression*</span><span class="sxs-lookup"><span data-stu-id="a7511-114">*Expression*</span></span>  <br/> |<span data-ttu-id="a7511-115">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="a7511-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7511-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7511-116">Remarks</span></span>

 <span data-ttu-id="a7511-117">**Try_Convert** leva o valor passado para ele e tenta convertê-lo para o *tipo de dados* de especificado.</span><span class="sxs-lookup"><span data-stu-id="a7511-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="a7511-118">Se a conversão for bem sucedido, o **Try_Convert** retornará o valor como o *tipo de dados* especificado; Se ocorrer um erro, null será retornado.</span><span class="sxs-lookup"><span data-stu-id="a7511-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="a7511-119">No entanto se você solicitar uma conversão que explicitamente não é permitida, **Try_Convert** falha com um erro.</span><span class="sxs-lookup"><span data-stu-id="a7511-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

