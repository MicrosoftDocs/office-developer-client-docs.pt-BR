---
title: Ação de Macro RequeryRecords (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Você pode usar a ação de RequeryRecords para atualizar, classificar e filtrar os dados no modo de exibição ativo repetindo a fonte do modo de exibição.
ms.openlocfilehash: 27c6a4f62f62f6d903de7a23d2aca6db8d316a84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765216"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a><span data-ttu-id="63f06-103">Ação de Macro RequeryRecords (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="63f06-103">RequeryRecords Macro Action (Access custom web app)</span></span>

<span data-ttu-id="63f06-104">Você pode usar a ação de **RequeryRecords** para atualizar, classificar e filtrar os dados no modo de exibição ativo repetindo a fonte do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="63f06-104">You can use the **RequeryRecords** action to refresh, sort, and filter the data in the active view by requerying the source of the view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="63f06-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="63f06-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="63f06-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="63f06-107">Setting</span></span>

<span data-ttu-id="63f06-108">A ação **RequeryRecords** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="63f06-108">The **RequeryRecords** action has the following arguments.</span></span> 
  
|<span data-ttu-id="63f06-109">**Parâmetro**</span><span class="sxs-lookup"><span data-stu-id="63f06-109">**Parameter**</span></span>|<span data-ttu-id="63f06-110">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="63f06-110">**Required**</span></span>|<span data-ttu-id="63f06-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="63f06-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63f06-112">**Onde =**</span><span class="sxs-lookup"><span data-stu-id="63f06-112">**Where=**</span></span> <br/> |<span data-ttu-id="63f06-113">Não</span><span class="sxs-lookup"><span data-stu-id="63f06-113">No</span></span>  <br/> |<span data-ttu-id="63f06-114">Uma cláusula SQL WHERE que restringe os registros no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="63f06-114">A SQL WHERE clause that restricts the records in the view.</span></span> <span data-ttu-id="63f06-115">Por padrão, esse argumento estiver em branco.</span><span class="sxs-lookup"><span data-stu-id="63f06-115">By default, this argument is blank.</span></span>  <br/> |
|<span data-ttu-id="63f06-116">**OrderBy**</span><span class="sxs-lookup"><span data-stu-id="63f06-116">**OrderBy**</span></span> <br/> |<span data-ttu-id="63f06-117">Não</span><span class="sxs-lookup"><span data-stu-id="63f06-117">No</span></span>  <br/> |<span data-ttu-id="63f06-118">Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais.</span><span class="sxs-lookup"><span data-stu-id="63f06-118">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="63f06-119">Por padrão, esse argumento estiver em branco.</span><span class="sxs-lookup"><span data-stu-id="63f06-119">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63f06-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="63f06-120">Remarks</span></span>

<span data-ttu-id="63f06-121">Qualquer classificação ou filtragem aplicada pelo usuário é limpa quando a ação **RequeryRecords** é chamada.</span><span class="sxs-lookup"><span data-stu-id="63f06-121">Any sorting or filtering applied by the user is cleared when the **RequeryRecords** action is called.</span></span> 
  
<span data-ttu-id="63f06-122">O argumento *OrderBy* é o nome do campo ou dos campos nos quais você deseja classificar os registros.</span><span class="sxs-lookup"><span data-stu-id="63f06-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="63f06-123">Quando você usa mais de um nome de campo, separe-os com vírgula (,).</span><span class="sxs-lookup"><span data-stu-id="63f06-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="63f06-124">Quando você define o argumento *OrderBy* , os registros são classificados por padrão em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="63f06-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  
<span data-ttu-id="63f06-125">Para classificar registros em ordem decrescente, digite DESC no final da expressão *OrderBy* argumento.</span><span class="sxs-lookup"><span data-stu-id="63f06-125">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression.</span></span> <span data-ttu-id="63f06-126">Por exemplo, para classificar registros em ordem decrescente por nome de contato do cliente, defina o argumento *OrderBy* para "ContactName DESC".</span><span class="sxs-lookup"><span data-stu-id="63f06-126">For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span></span> 
  
<span data-ttu-id="63f06-127">Para classificar os nomes por sobrenome em ordem decrescente e FirstName crescente, defina o argumento *OrderBy* como "DESC LastName, FirstName ASC".</span><span class="sxs-lookup"><span data-stu-id="63f06-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span></span> 
  

