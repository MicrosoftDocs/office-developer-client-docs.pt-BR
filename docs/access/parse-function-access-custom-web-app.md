---
title: Analisar a função (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analisa um valor de texto e retorna seu valor em um determinado tipo usando a cultura do aplicativo.
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765208"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="55c7b-103">Analisar a função (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="55c7b-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="55c7b-104">Analisa um valor de texto e retorna seu valor em um determinado tipo usando a cultura do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="55c7b-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="55c7b-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="55c7b-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="55c7b-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="55c7b-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="55c7b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55c7b-107">Syntax</span></span>

 <span data-ttu-id="55c7b-108">**Analisar** (*TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="55c7b-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="55c7b-109">A função **Analisar** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="55c7b-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="55c7b-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="55c7b-110">**Argument name**</span></span>|<span data-ttu-id="55c7b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="55c7b-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="55c7b-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="55c7b-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="55c7b-113">Uma expressão de texto representando o valor formatado para analisar em tipo de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="55c7b-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="55c7b-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="55c7b-114">*DataType*</span></span>  <br/> |<span data-ttu-id="55c7b-115">Valor literal que representa o tipo de dados solicitado para o resultado.</span><span class="sxs-lookup"><span data-stu-id="55c7b-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55c7b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="55c7b-116">Remarks</span></span>

<span data-ttu-id="55c7b-117">Use a **Analisar** apenas para a conversão de cadeia de caracteres, data/hora e tipos de número.</span><span class="sxs-lookup"><span data-stu-id="55c7b-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="55c7b-118">Para conversões de tipo geral, use a função **Converter** .</span><span class="sxs-lookup"><span data-stu-id="55c7b-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="55c7b-119">Tenha em mente que há um determinado desempenho sobrecarga na análise o valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="55c7b-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

