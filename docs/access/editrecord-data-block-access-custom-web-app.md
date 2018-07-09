---
title: Dados EditarRegistro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Você pode usar o bloco de dados EditarRegistro para alterar os valores contidos em um registro existente.
ms.openlocfilehash: 6c214e48326a93cff220b5436d7e7802cd6e3431
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765057"
---
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="15ed9-103">Dados EditarRegistro (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="15ed9-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="15ed9-104">Você pode usar o bloco de dados **EditarRegistro** para alterar os valores contidos em um registro existente.</span><span class="sxs-lookup"><span data-stu-id="15ed9-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="15ed9-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="15ed9-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="15ed9-107">O bloco de dados **EditarRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="15ed9-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="15ed9-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="15ed9-108">Setting</span></span>

<span data-ttu-id="15ed9-109">O bloco de dados **EditarRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="15ed9-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="15ed9-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="15ed9-110">**Argument**</span></span>|<span data-ttu-id="15ed9-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="15ed9-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15ed9-112">**Alias**</span><span class="sxs-lookup"><span data-stu-id="15ed9-112">**Alias**</span></span> <br/> |<span data-ttu-id="15ed9-113">Uma cadeia de caracteres que identifica o registro para editar.</span><span class="sxs-lookup"><span data-stu-id="15ed9-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="15ed9-114">Se o argumento *Alias* não for especificado, o registro atual é editado.</span><span class="sxs-lookup"><span data-stu-id="15ed9-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15ed9-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="15ed9-115">Remarks</span></span>

<span data-ttu-id="15ed9-116">Após a instrução **EditarRegistro** , você pode inserir um bloco de comandos que executará antes das alterações no registro forem confirmadas.</span><span class="sxs-lookup"><span data-stu-id="15ed9-116">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed.</span></span> <span data-ttu-id="15ed9-117">As ações a seguir estão disponíveis em um bloco de dados **EditarRegistro** .</span><span class="sxs-lookup"><span data-stu-id="15ed9-117">The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="15ed9-118">Ação de macro CancelRecordChange</span><span class="sxs-lookup"><span data-stu-id="15ed9-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="15ed9-119">Instrução de macro de comentário</span><span class="sxs-lookup"><span data-stu-id="15ed9-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="15ed9-120">Instrução de macro de grupo</span><span class="sxs-lookup"><span data-stu-id="15ed9-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="15ed9-121">Se... Então... Instrução de Macro Else</span><span class="sxs-lookup"><span data-stu-id="15ed9-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="15ed9-122">Ação de macro SetField</span><span class="sxs-lookup"><span data-stu-id="15ed9-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="15ed9-123">Ação de macro SetLocalVar</span><span class="sxs-lookup"><span data-stu-id="15ed9-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="15ed9-124">Use a ação **DefinirCampo** para especificar os novos valores de um campo no registro editado.</span><span class="sxs-lookup"><span data-stu-id="15ed9-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="15ed9-125">Você pode usar um **se … Então... Else** instrução para executar operações com base em uma condição.</span><span class="sxs-lookup"><span data-stu-id="15ed9-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="15ed9-p104">Para cancelar a edição de um registro, use a ação **CancelarAlteraçãodeRegistro**. Dessa forma, as alterações não são atribuídas e o bloco de dados **EditarRegistro** é encerrado.</span><span class="sxs-lookup"><span data-stu-id="15ed9-p104">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="15ed9-128">Você pode usar a variável local **IdentidadedeRegistroCriadapelaÚltimaVez** para executá-la com o último registro criado em um bloco de dados **CriarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="15ed9-128">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="15ed9-129">Por exemplo, use a sintaxe a seguir para se referir ao campo AssignedTo do registro mais recentemente criado:</span><span class="sxs-lookup"><span data-stu-id="15ed9-129">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


