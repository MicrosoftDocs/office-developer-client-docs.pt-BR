---
title: Bloco de dados CriarRegistro (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Você pode usar o bloco de dados CriarRegistro para criar um novo registro na tabela especificada.
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282247"
---
# <a name="createrecord-data-block-access-custom-web-app"></a><span data-ttu-id="b9c6d-103">Bloco de dados CriarRegistro (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="b9c6d-103">CreateRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="b9c6d-104">Você pode usar o bloco de dados **CriarRegistro** para criar um novo registro na tabela especificada.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b9c6d-p101">[!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b9c6d-107">O bloco de dados **CriarRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-107">The **CreateRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="b9c6d-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="b9c6d-108">Setting</span></span>

<span data-ttu-id="b9c6d-109">O bloco de dados **ExcluirRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-109">The **CreateRecord** data block has the following arguments.</span></span> 
  
<span data-ttu-id="b9c6d-110">O bloco de dados **ExcluirRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-110">The **CreateRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="b9c6d-111">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="b9c6d-111">**Argument name**</span></span>|<span data-ttu-id="b9c6d-112">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="b9c6d-112">**Required**</span></span>|<span data-ttu-id="b9c6d-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b9c6d-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b9c6d-114">**Criar Registro em**</span><span class="sxs-lookup"><span data-stu-id="b9c6d-114">**Create a Record In**</span></span> <br/> |<span data-ttu-id="b9c6d-115">Sim</span><span class="sxs-lookup"><span data-stu-id="b9c6d-115">Yes</span></span>  <br/> |<span data-ttu-id="b9c6d-116">O nome da tabela onde o novo registro será criado.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-116">The name of the table to create the new record in.</span></span>  <br/> |
|<span data-ttu-id="b9c6d-117">**Alias**</span><span class="sxs-lookup"><span data-stu-id="b9c6d-117">**Alias**</span></span> <br/> |<span data-ttu-id="b9c6d-118">Não</span><span class="sxs-lookup"><span data-stu-id="b9c6d-118">No</span></span>  <br/> |<span data-ttu-id="b9c6d-119">Uma cadeia de caracteres que identifica o registro.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-119">A string that identifies the record.</span></span> <span data-ttu-id="b9c6d-120">Você pode usar o alias do registro para identificá-lo</span><span class="sxs-lookup"><span data-stu-id="b9c6d-120">You can use the record's alias to identify</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9c6d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9c6d-121">Remarks</span></span>

<span data-ttu-id="b9c6d-122">O registro criado por **CriarRegistro** se torna automaticamente o registro atual.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-122">The record created by **CreateRecord** automatically becomes the current record.</span></span> 
  
<span data-ttu-id="b9c6d-123">Após \*\*\*\* a instrução CreateRecord, você pode inserir um bloco de comandos que será executado antes que o novo registro seja confirmado.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-123">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="b9c6d-124">As ações a seguir estão disponíveis em bloco de dados **CriarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-124">The following actions are available in a **CreateRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="b9c6d-125">Ação de macro CancelarAlteraçãodeRegistro</span><span class="sxs-lookup"><span data-stu-id="b9c6d-125">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="b9c6d-126">Instrução de macro de comentário</span><span class="sxs-lookup"><span data-stu-id="b9c6d-126">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="b9c6d-127">Instrução de macro de grupo</span><span class="sxs-lookup"><span data-stu-id="b9c6d-127">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="b9c6d-128">Instrução de macro Se...Então...Senão</span><span class="sxs-lookup"><span data-stu-id="b9c6d-128">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="b9c6d-129">Ação de macro SetField</span><span class="sxs-lookup"><span data-stu-id="b9c6d-129">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="b9c6d-130">Ação de macro SetLocalVar</span><span class="sxs-lookup"><span data-stu-id="b9c6d-130">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="b9c6d-131">Depois que a ação **CriarRegistro** criar um registro, use a ação **DefinirCampo** para especificar o valor de um campo no novo registro.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-131">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span> 
  
<span data-ttu-id="b9c6d-132">Você pode usar um **If... Then... Else** para executar operações com base em uma condição.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-132">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="b9c6d-p104">Para cancelar a criação de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **CriarRegistro** é encerrado.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-p104">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span> 
  
<span data-ttu-id="b9c6d-135">Quando o novo registro for atribuído, você poderá usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o registro.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-135">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="b9c6d-136">Por exemplo, use a sintaxe a seguir para se referir ao campo AssignedTo do Registro criado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-136">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


