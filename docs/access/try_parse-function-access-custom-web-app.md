---
title: Função Try_Parse (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analisa um valor de texto para o tipo de dados especificado na cultura do aplicativo ou retorna NULL se a conversão não for válida.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427525"
---
# <a name="tryparse-function-access-custom-web-app"></a><span data-ttu-id="fc0d0-103">Função Try_Parse (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="fc0d0-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="fc0d0-104">Analisa um valor de texto para o tipo de dados especificado na cultura do aplicativo ou retorna NULL se a conversão não for válida.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fc0d0-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="fc0d0-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="fc0d0-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="fc0d0-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fc0d0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc0d0-107">Syntax</span></span>

 <span data-ttu-id="fc0d0-108">**Try_Parse** (*Texté*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="fc0d0-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="fc0d0-109">A função **Try_Parse** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="fc0d0-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="fc0d0-110">**Argument name**</span></span>|<span data-ttu-id="fc0d0-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fc0d0-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fc0d0-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="fc0d0-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="fc0d0-113">Uma expressão de texto representando o valor formatado para analisar o tipo de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="fc0d0-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="fc0d0-114">*DataType*</span></span>  <br/> |<span data-ttu-id="fc0d0-115">O tipo de dados no qual a *textName* será analisada.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc0d0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc0d0-116">Remarks</span></span>

<span data-ttu-id="fc0d0-117">Use **Try_Parse** somente para conversão de cadeia de caracteres para tipos de data/hora e de número.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="fc0d0-118">Para conversões de tipo gerais, continue a usar **Convert**.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-118">For general type conversions, continue to use **Convert**.</span></span> 
  

