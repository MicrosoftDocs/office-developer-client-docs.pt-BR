---
title: Adesão a função (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Retorna a primeira expressão não for nula de uma lista de argumentos.
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765070"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="6cd27-103">Adesão a função (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="6cd27-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="6cd27-104">Retorna a primeira expressão não for nula de uma lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="6cd27-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6cd27-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="6cd27-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="6cd27-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="6cd27-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6cd27-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cd27-107">Syntax</span></span>

<span data-ttu-id="6cd27-108">**União** (*Valor*, [*valor*],..., [*valor*])</span><span class="sxs-lookup"><span data-stu-id="6cd27-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="6cd27-109">A função de **adesão** contém os seguintes argumentos</span><span class="sxs-lookup"><span data-stu-id="6cd27-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="6cd27-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="6cd27-110">**Argument name**</span></span>|<span data-ttu-id="6cd27-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6cd27-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6cd27-112">*Valor*</span><span class="sxs-lookup"><span data-stu-id="6cd27-112">*Value*</span></span>  <br/> |<span data-ttu-id="6cd27-113">Uma expressão.</span><span class="sxs-lookup"><span data-stu-id="6cd27-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cd27-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="6cd27-114">Remarks</span></span>

<span data-ttu-id="6cd27-115">Se todos os argumentos forem NULL, **adesão** retornará NULL.</span><span class="sxs-lookup"><span data-stu-id="6cd27-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6cd27-116">Example</span><span class="sxs-lookup"><span data-stu-id="6cd27-116">Example</span></span>

<span data-ttu-id="6cd27-117">A expressão a seguir é usada como a regra de validação para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="6cd27-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="6cd27-118">A expressão garante que as entradas são feitas nos campos nome, último nome, Email, telefone celular, trabalho, Home telefone, e companhia telefônica antes que um registro seja confirmado.</span><span class="sxs-lookup"><span data-stu-id="6cd27-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="6cd27-119">Se qualquer um dos campos listados forem deixadas em branco, a função de **adesão** retornará Null, o que viola a regra de validação.</span><span class="sxs-lookup"><span data-stu-id="6cd27-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


