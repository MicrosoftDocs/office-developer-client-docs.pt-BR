---
title: Função Coalesce (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Retorna a primeira expressão que não é NULL de uma lista de argumentos.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411390"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="56ac9-103">Função Coalesce (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="56ac9-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="56ac9-104">Retorna a primeira expressão que não é NULL de uma lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="56ac9-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="56ac9-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="56ac9-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="56ac9-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="56ac9-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="56ac9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56ac9-107">Syntax</span></span>

<span data-ttu-id="56ac9-108">**Coalesce** (*Valor*, [*Valor*], ...,[*Valor*])</span><span class="sxs-lookup"><span data-stu-id="56ac9-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="56ac9-109">A **função Coalesce** contém os seguintes argumentos</span><span class="sxs-lookup"><span data-stu-id="56ac9-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="56ac9-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="56ac9-110">**Argument name**</span></span>|<span data-ttu-id="56ac9-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="56ac9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="56ac9-112">*Valor*</span><span class="sxs-lookup"><span data-stu-id="56ac9-112">*Value*</span></span>  <br/> |<span data-ttu-id="56ac9-113">Uma expressão.</span><span class="sxs-lookup"><span data-stu-id="56ac9-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56ac9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="56ac9-114">Remarks</span></span>

<span data-ttu-id="56ac9-115">Se todos os argumentos são NULL, **Coalesce retorna** NULL.</span><span class="sxs-lookup"><span data-stu-id="56ac9-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="56ac9-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="56ac9-116">Example</span></span>

<span data-ttu-id="56ac9-117">A expressão a seguir é usada como regra de validação para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="56ac9-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="56ac9-118">A expressão garante que as entradas sejam feitas nos campos Nome, Sobrenome, Email, Telefone Celular, Telefone De Trabalho, Telefone Residência e Empresa antes da confirmação de um registro.</span><span class="sxs-lookup"><span data-stu-id="56ac9-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="56ac9-119">Se qualquer um dos campos listados for deixado em branco, a função **Coalesce** retornará Null, o que viola a regra de validação.</span><span class="sxs-lookup"><span data-stu-id="56ac9-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


