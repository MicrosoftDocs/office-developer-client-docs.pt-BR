---
title: Função Try_Parse (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analisa um valor de texto para o tipo de dados especificado na cultura do aplicativo ou retorna Null se a conversão não é válida.
ms.openlocfilehash: 3446e928d9772641f9aea7b956e142f995824b1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765248"
---
# <a name="tryparse-function-access-custom-web-app"></a><span data-ttu-id="ecb81-103">Função Try_Parse (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="ecb81-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="ecb81-104">Analisa um valor de texto para o tipo de dados especificado na cultura do aplicativo ou retorna Null se a conversão não é válida.</span><span class="sxs-lookup"><span data-stu-id="ecb81-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ecb81-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="ecb81-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="ecb81-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="ecb81-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ecb81-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ecb81-107">Syntax</span></span>

 <span data-ttu-id="ecb81-108">**Try_Parse** (*TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="ecb81-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="ecb81-109">A função **Try_Parse** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="ecb81-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ecb81-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="ecb81-110">**Argument name**</span></span>|<span data-ttu-id="ecb81-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ecb81-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ecb81-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="ecb81-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="ecb81-113">Uma expressão de texto representando o valor formatado para analisar em tipo de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="ecb81-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="ecb81-114">*Tipo de dados*</span><span class="sxs-lookup"><span data-stu-id="ecb81-114">*DataType*</span></span>  <br/> |<span data-ttu-id="ecb81-115">O tipo de dados no qual analisar *TextExpression* .</span><span class="sxs-lookup"><span data-stu-id="ecb81-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecb81-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ecb81-116">Remarks</span></span>

<span data-ttu-id="ecb81-117">Use **Try_Parse** apenas para a conversão de cadeia de caracteres, data/hora e tipos de número.</span><span class="sxs-lookup"><span data-stu-id="ecb81-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="ecb81-118">Para conversões de tipo geral, continue a usar a **Converter**.</span><span class="sxs-lookup"><span data-stu-id="ecb81-118">For general type conversions, continue to use **Convert**.</span></span> 
  

