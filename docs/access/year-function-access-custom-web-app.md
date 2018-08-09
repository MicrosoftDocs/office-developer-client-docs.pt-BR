---
title: Função Year (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Retorna um valor numérico que representa o ano da data especificada no calendário gregoriano.
ms.openlocfilehash: f9d72343637734257a2ed9589e5539b845933826
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765256"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="c3846-103">Função Year (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="c3846-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="c3846-104">Retorna um valor numérico que representa o ano da data especificada no calendário gregoriano.</span><span class="sxs-lookup"><span data-stu-id="c3846-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c3846-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="c3846-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="c3846-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="c3846-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c3846-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3846-107">Syntax</span></span>

 <span data-ttu-id="c3846-108">**Ano** (*Data*)</span><span class="sxs-lookup"><span data-stu-id="c3846-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="c3846-109">A função **Year** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c3846-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="c3846-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="c3846-110">**Argument name**</span></span>|<span data-ttu-id="c3846-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c3846-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c3846-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="c3846-112">*Date*</span></span>  <br/> |<span data-ttu-id="c3846-113">Uma expressão que pode ser resolvida como um valor de data/hora.</span><span class="sxs-lookup"><span data-stu-id="c3846-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="c3846-114">A expressão de argumento *Data* , expressão de coluna, a variável definida pelo usuário ou cadeia de caracteres literal.</span><span class="sxs-lookup"><span data-stu-id="c3846-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3846-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3846-115">Remarks</span></span>

<span data-ttu-id="c3846-116">Valores retornados pelas funções **ano**, **mês**e **dia** serão valores gregoriano independente do formato de exibição para o valor de data fornecida.</span><span class="sxs-lookup"><span data-stu-id="c3846-116">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value.</span></span> <span data-ttu-id="c3846-117">Por exemplo, se o formato de exibição dos usos data fornecida o calendário islâmico, os valores retornados para o **ano**, **mês**e **dia** funções serão ser valores associados à data gregoriano equivalente.</span><span class="sxs-lookup"><span data-stu-id="c3846-117">For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

