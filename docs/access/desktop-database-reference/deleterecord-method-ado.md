---
title: Método DeleteRecord (ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a91da1304d399a34f247eb251c2dadf0f1fa94d
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603004"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="f27a4-102">Método DeleteRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="f27a4-102">DeleteRecord Method (ADO)</span></span>


<span data-ttu-id="f27a4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f27a4-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="f27a4-104">Exclui a entidade representada por um [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f27a4-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f27a4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f27a4-105">Syntax</span></span>

<span data-ttu-id="f27a4-106">*Registro*. \**ExcluirRegistro \* \* \* fonte*, *assíncrono*</span><span class="sxs-lookup"><span data-stu-id="f27a4-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="f27a4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f27a4-107">Parameters</span></span>

  - <span data-ttu-id="f27a4-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="f27a4-108">*Source*</span></span>

  - <span data-ttu-id="f27a4-p101">Opcional. Um valor **String** que contém uma URL que identifica a entidade (por exemplo, o arquivo ou diretório) a ser excluída. Se *Source* for omitido ou especificar uma sequência vazia, a entidade representada pelo [Record](record-object-ado.md) atual será excluída. Se o Record for um registro de coleção ([RecordType](recordtype-property-ado.md) de **adCollectionRecord**, tal como um diretório) todos os filhos (por exemplo, subdiretórios) também serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="f27a4-p101">Optional. A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted. If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted. If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>

  - <span data-ttu-id="f27a4-113">*Async*</span><span class="sxs-lookup"><span data-stu-id="f27a4-113">*Async*</span></span>

  - <span data-ttu-id="f27a4-p102">Opcional. Um valor **Boolean** que, quando é **True**, especifica que a operação de exclusão é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f27a4-p102">Optional. A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>

## <a name="remarks"></a><span data-ttu-id="f27a4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f27a4-116">Remarks</span></span>

<span data-ttu-id="f27a4-p103">As operações no objeto representado por esse **Record** podem falhar após a conclusão desse método. Depois de chamar **DeleteRecord**, o **Record** deve ser fechado porque o comportamento do **Record** pode ficar imprevisível dependendo de quando o provedor atualiza o **Record** com a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="f27a4-p103">Operations on the object represented by this **Record** may fail after this method completes. After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="f27a4-119">Se esse **Record** foi obtido de um [Recordset](recordset-object-ado.md), os resultados dessa operação não serão refletidos imediatamente no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f27a4-119">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="f27a4-120">Atualize o **Recordset** fechando e abrindo-o novamente, ou os métodos **Recordset** [Requery](requery-method-ado.md), ou [Update](update-method-ado.md) e [Resync](resync-method-ado.md) executá-lo.</span><span class="sxs-lookup"><span data-stu-id="f27a4-120">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>


> [!NOTE]
<span data-ttu-id="f27a4-121"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="f27a4-121"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="f27a4-p105">[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs Absolutas e Relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="f27a4-p105">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="f27a4-124">[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="f27a4-124">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="f27a4-125">Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="f27a4-125">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="f27a4-126">mestre</span><span class="sxs-lookup"><span data-stu-id="f27a4-126">master</span></span>


