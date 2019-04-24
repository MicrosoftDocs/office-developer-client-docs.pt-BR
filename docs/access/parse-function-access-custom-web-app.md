---
title: Função Parse (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analisa um valor de texto e retorna seu valor em um determinado tipo usando a cultura do aplicativo.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308054"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="fa5ea-103">Função Parse (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="fa5ea-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="fa5ea-104">Analisa um valor de texto e retorna seu valor em um determinado tipo usando a cultura do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fa5ea-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fa5ea-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="fa5ea-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="fa5ea-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="fa5ea-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fa5ea-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa5ea-107">Syntax</span></span>

 <span data-ttu-id="fa5ea-108">**Parse** (*Texté*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="fa5ea-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="fa5ea-109">A função **Parse** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="fa5ea-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="fa5ea-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="fa5ea-110">**Argument name**</span></span>|<span data-ttu-id="fa5ea-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fa5ea-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fa5ea-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="fa5ea-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="fa5ea-113">Uma expressão de texto representando o valor formatado para analisar o tipo de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="fa5ea-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="fa5ea-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="fa5ea-114">*DataType*</span></span>  <br/> |<span data-ttu-id="fa5ea-115">Valor literal que representa o tipo de dados solicitado para o resultado.</span><span class="sxs-lookup"><span data-stu-id="fa5ea-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa5ea-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa5ea-116">Remarks</span></span>

<span data-ttu-id="fa5ea-117">Use **Parse** somente para conversão de cadeia de caracteres para tipos de data/hora e de número.</span><span class="sxs-lookup"><span data-stu-id="fa5ea-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="fa5ea-118">Para conversões de tipo gerais, use a função **Convert** .</span><span class="sxs-lookup"><span data-stu-id="fa5ea-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="fa5ea-119">Tenha em mente que há uma certa sobrecarga de desempenho na análise do valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fa5ea-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

