---
title: Método CopyRecord (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295524"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="ee153-102">Método CopyRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="ee153-102">CopyRecord method (ADO)</span></span>

<span data-ttu-id="ee153-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee153-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee153-104">Copia uma entidade representada por um **Record** para outro local.</span><span class="sxs-lookup"><span data-stu-id="ee153-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee153-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee153-105">Syntax</span></span>

<span data-ttu-id="ee153-106">*Registro*. CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="ee153-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="ee153-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee153-107">Parameters</span></span>

|<span data-ttu-id="ee153-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee153-108">Parameter</span></span>|<span data-ttu-id="ee153-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee153-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ee153-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="ee153-110">*Source*</span></span> |<span data-ttu-id="ee153-p101">Opcional. Um valor **String** que contém uma URL que especifica a entidade a ser copiada (por exemplo, um arquivo ou diretório). Se *Source* for omitido ou especificar uma sequência vazia, o arquivo ou diretório representado pelo [Record](record-object-ado.md) atual será copiado.</span><span class="sxs-lookup"><span data-stu-id="ee153-p101">Optional. A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory). If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>|
|<span data-ttu-id="ee153-114">*Destination*</span><span class="sxs-lookup"><span data-stu-id="ee153-114">*Destination*</span></span> |<span data-ttu-id="ee153-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ee153-115">Optional.</span></span> <span data-ttu-id="ee153-116">Um valor **String** que contém uma URL que especifica o local em que *Source* será copiado.</span><span class="sxs-lookup"><span data-stu-id="ee153-116">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>|
|<span data-ttu-id="ee153-117">*UserName*</span><span class="sxs-lookup"><span data-stu-id="ee153-117">*UserName*</span></span> |<span data-ttu-id="ee153-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ee153-118">Optional.</span></span> <span data-ttu-id="ee153-119">Um valor **String** que contém o ID de usuário que, se necessário, autoriza acesso ao *Destination*.</span><span class="sxs-lookup"><span data-stu-id="ee153-119">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="ee153-120">*Password*</span><span class="sxs-lookup"><span data-stu-id="ee153-120">*Password*</span></span> |<span data-ttu-id="ee153-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ee153-121">Optional.</span></span> <span data-ttu-id="ee153-122">Um valor **String** que contém a senha que, se necessária, verifica *UserName*.</span><span class="sxs-lookup"><span data-stu-id="ee153-122">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="ee153-123">*Options*</span><span class="sxs-lookup"><span data-stu-id="ee153-123">*Options*</span></span> |<span data-ttu-id="ee153-p105">Opcional. Um valor [CopyRecordOptionsEnum](copyrecordoptionsenum.md) que tem o valor padrão **adCopyUnspecified**. Especifica o comportamento deste método.</span><span class="sxs-lookup"><span data-stu-id="ee153-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="ee153-127">*Async*</span><span class="sxs-lookup"><span data-stu-id="ee153-127">*Async*</span></span> |<span data-ttu-id="ee153-p106">Opcional. Um valor **Boolean** que, quando é **True**, especifica que esta operação deve ser assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ee153-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="ee153-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ee153-130">Return value</span></span>

<span data-ttu-id="ee153-131">Um valor **String** que normalmente retorna o valor de *Destination*.</span><span class="sxs-lookup"><span data-stu-id="ee153-131">A **String** value that typically returns the value of *Destination*.</span></span> <span data-ttu-id="ee153-132">No entanto, o valor exato retornado depende do provedor.</span><span class="sxs-lookup"><span data-stu-id="ee153-132">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee153-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee153-133">Remarks</span></span>

<span data-ttu-id="ee153-p108">Os valores de *Source* e *Destination* não devem ser idênticos; caso contrário, ocorrerá um erro em tempo de execução. Pelo menos um dos nomes de servidor, caminho ou recurso deve ser diferente.</span><span class="sxs-lookup"><span data-stu-id="ee153-p108">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs. At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="ee153-p109">Todos os filhos (por exemplo, subdiretórios) de *Source* são copiados recursivamente, a menos que **adCopyNonRecursive** seja especificado. Em uma operação recursiva, *Destination* não deve ser um subdiretório de *Source*; caso contrário, a operação não será concluída.</span><span class="sxs-lookup"><span data-stu-id="ee153-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="ee153-138">Este método falha se *Destination* identificar uma entidade existente (por exemplo, um arquivo ou diretório), a menos que **adCopyOverWrite** seja especificado.</span><span class="sxs-lookup"><span data-stu-id="ee153-138">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee153-p110">Utilize a opção **adCopyOverWrite** criteriosamente. Por exemplo, especificar essa opção ao copiar um arquivo para um diretório irá *excluir* o diretório e substituí-lo pelo arquivo.</span><span class="sxs-lookup"><span data-stu-id="ee153-p110">Use the **adCopyOverWrite** option judiciously. For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>


> [!NOTE]
> <span data-ttu-id="ee153-141">[!OBSERVAçãO] URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="ee153-141">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="ee153-142">Para obter mais informações, consulte [URLs absolutas e relativas.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="ee153-142">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


