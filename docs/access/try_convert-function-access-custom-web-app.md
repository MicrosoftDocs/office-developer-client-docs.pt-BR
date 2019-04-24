---
title: Função Try_Convert (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Converte um valor em um tipo de dados especificado ou retorna NULL se a conversão não for válida.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304219"
---
# <a name="tryconvert-function-access-custom-web-app"></a><span data-ttu-id="5217f-103">Função Try_Convert (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="5217f-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="5217f-104">Converte um valor em um tipo de dados especificado ou retorna NULL se a conversão não for válida.</span><span class="sxs-lookup"><span data-stu-id="5217f-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5217f-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="5217f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5217f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5217f-107">Syntax</span></span>

 <span data-ttu-id="5217f-108">**Try_Convert** (*DataType*, *expression*)</span><span class="sxs-lookup"><span data-stu-id="5217f-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="5217f-109">A função **Try_Convert** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="5217f-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="5217f-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="5217f-110">**Argument name**</span></span>|<span data-ttu-id="5217f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5217f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5217f-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="5217f-112">*DataType*</span></span>  <br/> |<span data-ttu-id="5217f-113">O tipo de dados no qual a *expressão* será convertida.</span><span class="sxs-lookup"><span data-stu-id="5217f-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="5217f-114">*Expressão*.</span><span class="sxs-lookup"><span data-stu-id="5217f-114">*Expression*</span></span>  <br/> |<span data-ttu-id="5217f-115">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="5217f-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5217f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5217f-116">Remarks</span></span>

 <span data-ttu-id="5217f-117">**Try_Convert** leva o valor passado para ele e tenta convertê-lo para o *tipo de dados* especificado.</span><span class="sxs-lookup"><span data-stu-id="5217f-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="5217f-118">Se a conversão tiver êxito, **Try_Convert** retornará o valor como *DataType* especificado; Se ocorrer um erro, NULL será retornado.</span><span class="sxs-lookup"><span data-stu-id="5217f-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="5217f-119">No enTanto, se você solicitar uma conversão explicitamente não permitida, **Try_Convert** falhará com um erro.</span><span class="sxs-lookup"><span data-stu-id="5217f-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

