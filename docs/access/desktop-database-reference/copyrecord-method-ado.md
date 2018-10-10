---
title: Método CopyRecord (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a54cf5f4d14b3e623a576dee99e1fabeb070e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463714"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="017a5-102">Método CopyRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="017a5-102">CopyRecord Method (ADO)</span></span>


<span data-ttu-id="017a5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="017a5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="017a5-104">Copia uma entidade representada por um **Record** para outro local.</span><span class="sxs-lookup"><span data-stu-id="017a5-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="017a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="017a5-105">Syntax</span></span>

<span data-ttu-id="017a5-106">*Registro*. CopyRecord (*origem*, *destino*, *nome de usuário*, *senha*, *Opções*, *assíncrono*)</span><span class="sxs-lookup"><span data-stu-id="017a5-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="017a5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="017a5-107">Parameters</span></span>

  - <span data-ttu-id="017a5-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="017a5-108">*Source*</span></span>

  - <span data-ttu-id="017a5-109">Opcional.</span><span class="sxs-lookup"><span data-stu-id="017a5-109">Optional.</span></span> <span data-ttu-id="017a5-110">Um valor **String** que contém uma URL que especifica a entidade a ser copiada (por exemplo, um arquivo ou diretório).</span><span class="sxs-lookup"><span data-stu-id="017a5-110">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="017a5-111">Se a *fonte* for omitido ou especifica uma sequência vazia, o arquivo ou diretório representado pelo [registro](record-object-ado.md) atual será copiado.</span><span class="sxs-lookup"><span data-stu-id="017a5-111">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>

  - <span data-ttu-id="017a5-112">*Destination*</span><span class="sxs-lookup"><span data-stu-id="017a5-112">*Destination*</span></span>

  - <span data-ttu-id="017a5-113">Opcional.</span><span class="sxs-lookup"><span data-stu-id="017a5-113">Optional.</span></span> <span data-ttu-id="017a5-114">Um valor **String** que contém uma URL, especificando o local onde *fonte* serão copiados.</span><span class="sxs-lookup"><span data-stu-id="017a5-114">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>

  - <span data-ttu-id="017a5-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="017a5-115">*UserName*</span></span>

  - <span data-ttu-id="017a5-p103">Opcional. Um valor **String** que contém o ID de usuário que, se necessário, autoriza acesso ao *Destination*.</span><span class="sxs-lookup"><span data-stu-id="017a5-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="017a5-118">*Password*</span><span class="sxs-lookup"><span data-stu-id="017a5-118">*Password*</span></span>

  - <span data-ttu-id="017a5-p104">Opcional. Um valor **String** que contém a senha que, se necessária, verifica *UserName*.</span><span class="sxs-lookup"><span data-stu-id="017a5-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="017a5-121">*Options*</span><span class="sxs-lookup"><span data-stu-id="017a5-121">*Options*</span></span>

  - <span data-ttu-id="017a5-p105">Opcional. Um valor [CopyRecordOptionsEnum](copyrecordoptionsenum.md) que tem o valor padrão **adCopyUnspecified**. Especifica o comportamento deste método.</span><span class="sxs-lookup"><span data-stu-id="017a5-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="017a5-125">*Async*</span><span class="sxs-lookup"><span data-stu-id="017a5-125">*Async*</span></span>

  - <span data-ttu-id="017a5-p106">Opcional. Um valor **Boolean** que, quando é **True**, especifica que esta operação deve ser assíncrona.</span><span class="sxs-lookup"><span data-stu-id="017a5-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>

## <a name="return-value"></a><span data-ttu-id="017a5-128">Valor de Retorno</span><span class="sxs-lookup"><span data-stu-id="017a5-128">Return Value</span></span>

<span data-ttu-id="017a5-p107">Um valor **String** que normalmente retorna o valor de *Destination*. No entanto, o valor exato retornado depende do provedor.</span><span class="sxs-lookup"><span data-stu-id="017a5-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="017a5-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="017a5-131">Remarks</span></span>

<span data-ttu-id="017a5-132">Os valores de *origem* e de *destino* não devem ser idênticos; Caso contrário, ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="017a5-132">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="017a5-133">Pelo menos um dos nomes de servidor, caminho ou recurso deve ser diferente.</span><span class="sxs-lookup"><span data-stu-id="017a5-133">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="017a5-p109">Todos os filhos (por exemplo, subdiretórios) de *Source* são copiados recursivamente, a menos que **adCopyNonRecursive** seja especificado. Em uma operação recursiva, *Destination* não deve ser um subdiretório de *Source*; caso contrário, a operação não será concluída.</span><span class="sxs-lookup"><span data-stu-id="017a5-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="017a5-136">Este método falha se *Destination* identificar uma entidade existente (por exemplo, um arquivo ou diretório), a menos que **adCopyOverWrite** seja especificado.</span><span class="sxs-lookup"><span data-stu-id="017a5-136">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>


> [!IMPORTANT]
> <P><span data-ttu-id="017a5-137">[!IMPORTANTE] Utilize a opção <STRONG>adCopyOverWrite</STRONG> criteriosamente.</span><span class="sxs-lookup"><span data-stu-id="017a5-137">Use the <STRONG>adCopyOverWrite</STRONG> option judiciously.</span></span> <span data-ttu-id="017a5-138">Por exemplo, se você especificar essa opção ao copiar um arquivo em um diretório irá <EM>Excluir</EM> o diretório e substituí-lo com o arquivo.</span><span class="sxs-lookup"><span data-stu-id="017a5-138">For example, specifying this option when copying a file to a directory will <EM>delete</EM> the directory and replace it with the file.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="017a5-p111">[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs Absolutas e Relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="017a5-p111">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


