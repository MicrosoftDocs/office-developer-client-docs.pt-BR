---
title: Método MoveRecord (ADO)
TOCTitle: MoveRecord Method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6955bca1bf693386d1f5edb4bac04cee311d78e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606959"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="fc985-102">Método MoveRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="fc985-102">MoveRecord Method (ADO)</span></span>


<span data-ttu-id="fc985-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc985-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="fc985-104">Move a entidade representada por um [Record](record-object-ado.md) para outro local.</span><span class="sxs-lookup"><span data-stu-id="fc985-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc985-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc985-105">Syntax</span></span>

<span data-ttu-id="fc985-106">*Registro*. MoveRecord (*origem*, *destino*, *nome de usuário*, *senha*, *Opções*, *assíncrono*)</span><span class="sxs-lookup"><span data-stu-id="fc985-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="fc985-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc985-107">Parameters</span></span>

  - <span data-ttu-id="fc985-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="fc985-108">*Source*</span></span>

  - <span data-ttu-id="fc985-p101">Opcional. Um valor **String** que contém uma URL que identifica o **Record** a ser movido. Se *Source* for omitido ou especificar uma sequência vazia, o objeto representado por este **Record** será movido. Por exemplo, se o **Record** representar um arquivo, o conteúdo do arquivo será movido para o local especificado por *Destination*.</span><span class="sxs-lookup"><span data-stu-id="fc985-p101">Optional. A **String** value that contains a URL identifying the **Record** to be moved. If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved. For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>

  - <span data-ttu-id="fc985-113">*Destination*</span><span class="sxs-lookup"><span data-stu-id="fc985-113">*Destination*</span></span>

  - <span data-ttu-id="fc985-114">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fc985-114">Optional.</span></span> <span data-ttu-id="fc985-115">Um valor **String** que contém uma URL, especificando o local onde *fonte* será movido.</span><span class="sxs-lookup"><span data-stu-id="fc985-115">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>

  - <span data-ttu-id="fc985-116">*UserName*</span><span class="sxs-lookup"><span data-stu-id="fc985-116">*UserName*</span></span>

  - <span data-ttu-id="fc985-p103">Opcional. Um valor **String** que contém o ID de usuário que, se necessário, autoriza acesso ao *Destination*.</span><span class="sxs-lookup"><span data-stu-id="fc985-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="fc985-119">*Password*</span><span class="sxs-lookup"><span data-stu-id="fc985-119">*Password*</span></span>

  - <span data-ttu-id="fc985-p104">Opcional. Uma **String** que contém a senha que, se necessária, verifica *UserName*.</span><span class="sxs-lookup"><span data-stu-id="fc985-p104">Optional. A **String** that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="fc985-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="fc985-122">*Options*</span></span>

  - <span data-ttu-id="fc985-p105">Opcional. Um valor [MoveRecordOptionsEnum](moverecordoptionsenum.md) cujo valor padrão é **adMoveUnspecified**. Especifica o comportamento deste método.</span><span class="sxs-lookup"><span data-stu-id="fc985-p105">Optional. A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="fc985-126">*Async*</span><span class="sxs-lookup"><span data-stu-id="fc985-126">*Async*</span></span>

  - <span data-ttu-id="fc985-p106">Opcional. Um valor **Boolean** que, quando é **True**, especifica que esta operação deve ser assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fc985-p106">Optional. A **Boolean** value that, when **True**, specifies this operation should be asynchronous .</span></span>

<span data-ttu-id="fc985-129"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="fc985-129"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="fc985-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fc985-130">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="fc985-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fc985-131">Return value</span></span>
>>>>>>> <span data-ttu-id="fc985-132">mestre</span><span class="sxs-lookup"><span data-stu-id="fc985-132">master</span></span>

<span data-ttu-id="fc985-133">Um valor **String**.</span><span class="sxs-lookup"><span data-stu-id="fc985-133">A **String** value.</span></span> <span data-ttu-id="fc985-134">Geralmente, é retornado o valor de *destino* .</span><span class="sxs-lookup"><span data-stu-id="fc985-134">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="fc985-135">No entanto, o valor exato retornado depende do provedor.</span><span class="sxs-lookup"><span data-stu-id="fc985-135">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc985-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc985-136">Remarks</span></span>

<span data-ttu-id="fc985-137">Os valores de *origem* e de *destino* não devem ser idênticos; Caso contrário, ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="fc985-137">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="fc985-138">Pelo menos os nomes de servidor, caminho e recurso devem ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="fc985-138">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="fc985-p109">Para arquivos movidos utilizando-se o Internet Publishing Provider, este método atualiza todos os links de hipertexto nos arquivos que estão sendo movidos, a menos que especificado o contrário por *Options*. Este método falha se *Destination* identificar um objeto existente (por exemplo, um arquivo ou diretório), a menos que **adMoveOverWrite** seja especificado.</span><span class="sxs-lookup"><span data-stu-id="fc985-p109">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*. This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fc985-p110">[!OBSERVAçãO] Utilize a opção <STRONG>adMoveOverWrite</STRONG> criteriosamente. Por exemplo, especificar essa opção ao mover um arquivo para um diretório irá excluir o diretório e substituí-lo pelo arquivo.</span><span class="sxs-lookup"><span data-stu-id="fc985-p110">Use the <STRONG>adMoveOverWrite</STRONG> option judiciously. For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span></P>



<span data-ttu-id="fc985-p111">Alguns atributos do objeto **Record**, tal como a propriedade [ParentURL](parenturl-property-ado.md), não serão atualizados após a conclusão dessa operação. Atualize as propriedades do objeto **Record** fechando o **Record** e, em seguida, reabrindo-o com a URL do local em que o arquivo ou diretório foi movido.</span><span class="sxs-lookup"><span data-stu-id="fc985-p111">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="fc985-p112">Se esse **Record** foi obtido de um [Recordset](recordset-object-ado.md), o novo local do arquivo ou diretório movido não será refletido imediatamente no **Recordset**. Atualize o **Recordset** fechando e reabrindo o mesmo.</span><span class="sxs-lookup"><span data-stu-id="fc985-p112">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**. Refresh the **Recordset** by closing and re-opening it.</span></span>


> [!NOTE]
<span data-ttu-id="fc985-147"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="fc985-147"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="fc985-p113">[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs Absolutas e Relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="fc985-p113">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="fc985-150">[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="fc985-150">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="fc985-151">Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="fc985-151">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="fc985-152">mestre</span><span class="sxs-lookup"><span data-stu-id="fc985-152">master</span></span>


