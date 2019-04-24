---
title: Ação de macro OpenPopup (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Abre o modo de exibição especificado em uma janela pop-up.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308110"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="c30ea-103">Ação de macro OpenPopup (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="c30ea-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="c30ea-104">Abre o modo de exibição especificado em uma janela pop-up.</span><span class="sxs-lookup"><span data-stu-id="c30ea-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c30ea-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="c30ea-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c30ea-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c30ea-107">Syntax</span></span>

 <span data-ttu-id="c30ea-108">**OpenPopup** (*Exibir*, *onde =*, *ordenar por*)</span><span class="sxs-lookup"><span data-stu-id="c30ea-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="c30ea-109">A ação **OpenPopup** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c30ea-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="c30ea-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="c30ea-110">**Argument name**</span></span>|<span data-ttu-id="c30ea-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c30ea-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c30ea-112">*View*</span><span class="sxs-lookup"><span data-stu-id="c30ea-112">*View*</span></span>  <br/> |<span data-ttu-id="c30ea-113">O nome do modo de exibição que será aberto.</span><span class="sxs-lookup"><span data-stu-id="c30ea-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="c30ea-114">*Onde =*</span><span class="sxs-lookup"><span data-stu-id="c30ea-114">*Where=*</span></span>  <br/> |<span data-ttu-id="c30ea-115">Uma cláusula SQL WHERE válida (sem a palavra WHERE) que restringe os registros no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="c30ea-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="c30ea-116">*Classificado Por*</span><span class="sxs-lookup"><span data-stu-id="c30ea-116">*Order By*</span></span>  <br/> |<span data-ttu-id="c30ea-117">Uma expressão de cadeia de caracteres que inclui o nome do(s) campo(s) no(s) qual(is) serão classificados os registros e as palavras-chave CRESC ou DECRESC opcionais.</span><span class="sxs-lookup"><span data-stu-id="c30ea-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="c30ea-118">Por padrão, esse argumento fica em branco.</span><span class="sxs-lookup"><span data-stu-id="c30ea-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c30ea-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c30ea-119">Remarks</span></span>

<span data-ttu-id="c30ea-120">A macro atual terminará quando a ação **OpenPopup** for processada.</span><span class="sxs-lookup"><span data-stu-id="c30ea-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="c30ea-121">Qualquer classificação ou filtragem aplicada pelo usuário é desmarcada quando a ação **OpenPopup** é chamada.</span><span class="sxs-lookup"><span data-stu-id="c30ea-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="c30ea-122">O argumento *OrderBy* é o nome do campo ou dos campos nos quais você deseja classificar registros.</span><span class="sxs-lookup"><span data-stu-id="c30ea-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="c30ea-123">Quando você usa mais de um nome de campo, separe-os com uma vírgula (,).</span><span class="sxs-lookup"><span data-stu-id="c30ea-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="c30ea-124">Quando você define o argumento *OrderBy* , os registros são classificados por padrão em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="c30ea-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

