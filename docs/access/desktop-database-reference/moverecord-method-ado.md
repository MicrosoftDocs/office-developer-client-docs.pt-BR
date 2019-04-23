---
title: Método MoveRecord (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9937f0ab32c5dba0e4435fdc0ba7e111f5651dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288676"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="410bc-102">Método MoveRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="410bc-102">MoveRecord method (ADO)</span></span>

<span data-ttu-id="410bc-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="410bc-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="410bc-104">Move a entidade representada por um [Record](record-object-ado.md) para outro local.</span><span class="sxs-lookup"><span data-stu-id="410bc-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="410bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="410bc-105">Syntax</span></span>

<span data-ttu-id="410bc-106">*Record*. MoveRecord (*origem*, *destino*, *nome de usuário*, *senha*, *Opções*, *assíncrono*)</span><span class="sxs-lookup"><span data-stu-id="410bc-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="410bc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="410bc-107">Parameters</span></span>

|<span data-ttu-id="410bc-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="410bc-108">Parameter</span></span>|<span data-ttu-id="410bc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="410bc-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="410bc-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="410bc-110">*Source*</span></span> |<span data-ttu-id="410bc-p101">Opcional. Um valor **String** que contém uma URL que identifica o **Record** a ser movido. Se *Source* for omitido ou especificar uma sequência vazia, o objeto representado por este **Record** será movido. Por exemplo, se o **Record** representar um arquivo, o conteúdo do arquivo será movido para o local especificado por *Destination*.</span><span class="sxs-lookup"><span data-stu-id="410bc-p101">Optional. A **String** value that contains a URL identifying the **Record** to be moved. If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved. For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>|
|<span data-ttu-id="410bc-115">*Destination*</span><span class="sxs-lookup"><span data-stu-id="410bc-115">*Destination*</span></span> |<span data-ttu-id="410bc-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="410bc-116">Optional.</span></span> <span data-ttu-id="410bc-117">Um valor **String** que contém uma URL que especifica o local em que *Source* será movido.</span><span class="sxs-lookup"><span data-stu-id="410bc-117">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>|
|<span data-ttu-id="410bc-118">*UserName*</span><span class="sxs-lookup"><span data-stu-id="410bc-118">*UserName*</span></span> |<span data-ttu-id="410bc-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="410bc-119">Optional.</span></span> <span data-ttu-id="410bc-120">Um valor **String** que contém o ID de usuário que, se necessário, autoriza acesso ao *Destination*.</span><span class="sxs-lookup"><span data-stu-id="410bc-120">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="410bc-121">*Password*</span><span class="sxs-lookup"><span data-stu-id="410bc-121">*Password*</span></span> |<span data-ttu-id="410bc-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="410bc-122">Optional.</span></span> <span data-ttu-id="410bc-123">Uma **String** que contém a senha que, se necessária, verifica *UserName*.</span><span class="sxs-lookup"><span data-stu-id="410bc-123">A **String** that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="410bc-124">*Options*</span><span class="sxs-lookup"><span data-stu-id="410bc-124">*Options*</span></span> |<span data-ttu-id="410bc-p105">Opcional. Um valor [MoveRecordOptionsEnum](moverecordoptionsenum.md) cujo valor padrão é **adMoveUnspecified**. Especifica o comportamento deste método.</span><span class="sxs-lookup"><span data-stu-id="410bc-p105">Optional. A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="410bc-128">*Async*</span><span class="sxs-lookup"><span data-stu-id="410bc-128">*Async*</span></span> |<span data-ttu-id="410bc-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="410bc-129">Optional.</span></span> <span data-ttu-id="410bc-130">Um valor **Boolean** que, quando **true**, especifica que esta operação deve ser assíncrona.</span><span class="sxs-lookup"><span data-stu-id="410bc-130">A **Boolean** value that, when **True**, specifies this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="410bc-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="410bc-131">Return value</span></span>

<span data-ttu-id="410bc-132">Um valor **String**.</span><span class="sxs-lookup"><span data-stu-id="410bc-132">A **String** value.</span></span> <span data-ttu-id="410bc-133">Normalmente, o valor de *Destination* é retornado.</span><span class="sxs-lookup"><span data-stu-id="410bc-133">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="410bc-134">No entanto, o valor exato retornado depende do provedor.</span><span class="sxs-lookup"><span data-stu-id="410bc-134">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="410bc-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="410bc-135">Remarks</span></span>

<span data-ttu-id="410bc-p108">Os valores de *Source* e *Destination* não devem ser idênticos; caso contrário, ocorrerá um erro em tempo de execução. Pelo menos os nomes de servidor, caminho e recurso devem ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="410bc-p108">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs. At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="410bc-p109">Para arquivos movidos utilizando-se o Internet Publishing Provider, este método atualiza todos os links de hipertexto nos arquivos que estão sendo movidos, a menos que especificado o contrário por *Options*. Este método falha se *Destination* identificar um objeto existente (por exemplo, um arquivo ou diretório), a menos que **adMoveOverWrite** seja especificado.</span><span class="sxs-lookup"><span data-stu-id="410bc-p109">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*. This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>

> [!NOTE]
> <span data-ttu-id="410bc-p110">[!OBSERVAçãO] Utilize a opção **adMoveOverWrite** criteriosamente. Por exemplo, especificar essa opção ao mover um arquivo para um diretório irá excluir o diretório e substituí-lo pelo arquivo.</span><span class="sxs-lookup"><span data-stu-id="410bc-p110">Use the **adMoveOverWrite** option judiciously. For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span>

<span data-ttu-id="410bc-p111">Alguns atributos do objeto **Record**, tal como a propriedade [ParentURL](parenturl-property-ado.md), não serão atualizados após a conclusão dessa operação. Atualize as propriedades do objeto **Record** fechando o **Record** e, em seguida, reabrindo-o com a URL do local em que o arquivo ou diretório foi movido.</span><span class="sxs-lookup"><span data-stu-id="410bc-p111">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="410bc-p112">Se esse **Record** foi obtido de um [Recordset](recordset-object-ado.md), o novo local do arquivo ou diretório movido não será refletido imediatamente no **Recordset**. Atualize o **Recordset** fechando e reabrindo o mesmo.</span><span class="sxs-lookup"><span data-stu-id="410bc-p112">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**. Refresh the **Recordset** by closing and re-opening it.</span></span>

> [!NOTE]
> <span data-ttu-id="410bc-146">[!OBSERVAçãO] URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="410bc-146">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="410bc-147">Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="410bc-147">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


