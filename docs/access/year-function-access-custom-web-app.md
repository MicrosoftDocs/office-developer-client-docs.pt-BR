---
title: Função Year (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Retorna um valor numérico que representa o ano da data especificada no calendário gregoriano.
ms.openlocfilehash: 1400c352bcc070035d15b46f8e547e4637364299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433119"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="6eca0-103">Função Year (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="6eca0-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="6eca0-104">Retorna um valor numérico que representa o ano da data especificada no calendário gregoriano.</span><span class="sxs-lookup"><span data-stu-id="6eca0-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6eca0-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="6eca0-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="6eca0-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="6eca0-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6eca0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6eca0-107">Syntax</span></span>

 <span data-ttu-id="6eca0-108">**Ano** (*Data*)</span><span class="sxs-lookup"><span data-stu-id="6eca0-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="6eca0-109">A função **year** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="6eca0-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="6eca0-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="6eca0-110">**Argument name**</span></span>|<span data-ttu-id="6eca0-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6eca0-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6eca0-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="6eca0-112">*Date*</span></span>  <br/> |<span data-ttu-id="6eca0-113">Uma expressão que pode ser resolvida como um valor de data/hora.</span><span class="sxs-lookup"><span data-stu-id="6eca0-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="6eca0-114">A expressão de argumento de *Data* , expressão de coluna, variável definida pelo usuário ou literal de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6eca0-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6eca0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6eca0-115">Remarks</span></span>

<span data-ttu-id="6eca0-116">Os valores retornados pelas funções **ano**, **mês**e **dia** serão valores gregorianos, independentemente do formato de exibição para o valor de data fornecido.</span><span class="sxs-lookup"><span data-stu-id="6eca0-116">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value.</span></span> <span data-ttu-id="6eca0-117">Por exemplo, se o formato de exibição da data fornecida usar o calendário islâmico, os valores retornados para as funções **ano**, **mês**e **dia** serão valores associados à data gregoriana equivalente.</span><span class="sxs-lookup"><span data-stu-id="6eca0-117">For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

