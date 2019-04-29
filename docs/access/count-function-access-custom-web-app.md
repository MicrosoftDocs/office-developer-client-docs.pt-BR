---
title: Função Count (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Retorna o número de registros em uma consulta ou tabela.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419139"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="b3a1a-103">Função Count (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="b3a1a-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="b3a1a-104">Retorna o número de registros em uma consulta ou tabela.</span><span class="sxs-lookup"><span data-stu-id="b3a1a-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b3a1a-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="b3a1a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b3a1a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3a1a-107">Syntax</span></span>

<span data-ttu-id="b3a1a-108">**Contagem** (*Expressão*)</span><span class="sxs-lookup"><span data-stu-id="b3a1a-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="b3a1a-109">A função **Count** contém o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="b3a1a-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="b3a1a-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="b3a1a-110">**Argument name**</span></span>|<span data-ttu-id="b3a1a-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b3a1a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b3a1a-112">*Expressão*</span><span class="sxs-lookup"><span data-stu-id="b3a1a-112">*Expression*</span></span>  <br/> |<span data-ttu-id="b3a1a-113">Uma expressão de cadeia de caracteres identificando o campo que contém os dados que você deseja contar ou uma expressão que executa um cálculo usando os dados no campo.</span><span class="sxs-lookup"><span data-stu-id="b3a1a-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="b3a1a-114">Os operandos na *expressão* podem incluir o nome de um campo de tabela ou função (que pode ser intrínseco ou definido pelo usuário, mas não outras funções de agregação SQL).</span><span class="sxs-lookup"><span data-stu-id="b3a1a-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="b3a1a-115">É possível contar qualquer tipo de dados, inclusive texto.</span><span class="sxs-lookup"><span data-stu-id="b3a1a-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3a1a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3a1a-116">Remarks</span></span>

<span data-ttu-id="b3a1a-117">Você pode usar Count para contar o número de registros em uma consulta de base.</span><span class="sxs-lookup"><span data-stu-id="b3a1a-117">You can use Count to count the number of records in an underlying query.</span></span> <span data-ttu-id="b3a1a-118">Por exemplo, você poderia usar Count para contar o número de pedidos enviados para um determinado país ou região.</span><span class="sxs-lookup"><span data-stu-id="b3a1a-118">For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="b3a1a-119">**Contagem** (\*) retorna o número de itens em um grupo.</span><span class="sxs-lookup"><span data-stu-id="b3a1a-119">**Count** (\*) returns the number of items in a group.</span></span> <span data-ttu-id="b3a1a-120">Isso inclui valores nulos e duplicatas.</span><span class="sxs-lookup"><span data-stu-id="b3a1a-120">This includes NULL values and duplicates.</span></span> 
  

