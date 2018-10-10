---
title: Método Open (Record do ADO)
TOCTitle: Open Method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d56fbf28cd878a8a8fd803bf550d81bc9ac2c96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462478"
---
# <a name="open-method-ado-record"></a><span data-ttu-id="90438-102">Método Open (Record do ADO)</span><span class="sxs-lookup"><span data-stu-id="90438-102">Open Method (ADO Record)</span></span>


<span data-ttu-id="90438-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="90438-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="90438-104">Abre um objeto [Record](record-object-ado.md) existente ou cria um novo item representado pelo **Record** (tal como um arquivo ou diretório).</span><span class="sxs-lookup"><span data-stu-id="90438-104">Opens an existing [Record](record-object-ado.md) object, or creates a new item represented by the **Record** (such as a file or directory).</span></span>

## <a name="syntax"></a><span data-ttu-id="90438-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90438-105">Syntax</span></span>

<span data-ttu-id="90438-106">Abra a *fonte*, *ActiveConnection*, *modo*, *CreateOptions*, *Opções*, *nome de usuário*, *senha*</span><span class="sxs-lookup"><span data-stu-id="90438-106">Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*</span></span>

## <a name="parameters"></a><span data-ttu-id="90438-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90438-107">Parameters</span></span>

  - <span data-ttu-id="90438-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="90438-108">*Source*</span></span>

  - <span data-ttu-id="90438-p101">Opcional. Uma **Variant** que pode representar a URL da entidade a ser representada por esse objeto **Record**, um **Command**, um [Recordset](recordset-object-ado.md) aberto ou outro objeto **Record**, uma sequência que contém uma instrução SQL SELECT ou um nome de tabela.</span><span class="sxs-lookup"><span data-stu-id="90438-p101">Optional. A **Variant** that may represent the URL of the entity to be represented by this **Record** object, a **Command**, an open [Recordset](recordset-object-ado.md) or another **Record** object, a string containing a SQL SELECT statement or a table name.</span></span>

  - <span data-ttu-id="90438-111">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="90438-111">*ActiveConnection*</span></span>

  - <span data-ttu-id="90438-p102">Opcional. Uma **Variant** que representa a sequência de conexão ou objeto [Connection](connection-object-ado.md) aberto.</span><span class="sxs-lookup"><span data-stu-id="90438-p102">Optional. A **Variant** that represents the connect string or open [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="90438-114">*Mode*</span><span class="sxs-lookup"><span data-stu-id="90438-114">*Mode*</span></span>

  - <span data-ttu-id="90438-p103">Opcional. Um valor [ConnectModeEnum](connectmodeenum.md), cujo valor padrão é **adModeUnknown**, que especifica o modo de acesso para o objeto **Record** resultante.</span><span class="sxs-lookup"><span data-stu-id="90438-p103">Optional. A [ConnectModeEnum](connectmodeenum.md) value, whose default value is **adModeUnknown**, that specifies the access mode for the resultant **Record** object.</span></span>

  - <span data-ttu-id="90438-117">*CreateOptions*</span><span class="sxs-lookup"><span data-stu-id="90438-117">*CreateOptions*</span></span>

  - <span data-ttu-id="90438-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="90438-118">Optional.</span></span> <span data-ttu-id="90438-119">Um valor [RecordCreateOptionsEnum](recordcreateoptionsenum.md), cujo valor padrão é **adFailIfNotExists**, que especifica se um arquivo ou diretório existente deve ser aberto ou se um novo arquivo ou diretório deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="90438-119">A [RecordCreateOptionsEnum](recordcreateoptionsenum.md) value, whose default value is **adFailIfNotExists**, that specifies whether an existing file or directory should be opened, or a new file or directory should be created.</span></span> <span data-ttu-id="90438-120">Se definido para o valor padrão, o modo de acesso será obtido da propriedade [Mode](mode-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="90438-120">If set to the default value, the access mode is obtained from the [Mode](mode-property-ado.md) property.</span></span> <span data-ttu-id="90438-121">Esse parâmetro é ignorado quando o parâmetro *Source* não contém uma URL.</span><span class="sxs-lookup"><span data-stu-id="90438-121">This parameter is ignored when the *Source* parameter doesnt contain a URL.</span></span>

  - <span data-ttu-id="90438-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="90438-122">*Options*</span></span>

  - <span data-ttu-id="90438-p105">Opcional. Um valor [RecordOpenOptionsEnum](recordopenoptionsenum.md), cujo valor padrão é **adOpenRecordUnspecified**, que especifica opções para a abertura do **Record**. Esses valores podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="90438-p105">Optional. A [RecordOpenOptionsEnum](recordopenoptionsenum.md) value, whose default value is **adOpenRecordUnspecified**, that specifies options for opening the **Record**. These values may be combined.</span></span>

  - <span data-ttu-id="90438-126">*UserName*</span><span class="sxs-lookup"><span data-stu-id="90438-126">*UserName*</span></span>

  - <span data-ttu-id="90438-p106">Opcional. Um valor **String** que contém o ID de usuário que, se necessário, autoriza acesso a *Source*.</span><span class="sxs-lookup"><span data-stu-id="90438-p106">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Source*.</span></span>

  - <span data-ttu-id="90438-129">*Password*</span><span class="sxs-lookup"><span data-stu-id="90438-129">*Password*</span></span>

  - <span data-ttu-id="90438-p107">Opcional. Um valor **String** que contém a senha que, se necessária, verifica *UserName*.</span><span class="sxs-lookup"><span data-stu-id="90438-p107">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

## <a name="remarks"></a><span data-ttu-id="90438-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="90438-132">Remarks</span></span>

<span data-ttu-id="90438-133">*Source* pode ser:</span><span class="sxs-lookup"><span data-stu-id="90438-133">*Source* may be:</span></span>

  - <span data-ttu-id="90438-134">Uma URL.</span><span class="sxs-lookup"><span data-stu-id="90438-134">A URL.</span></span> <span data-ttu-id="90438-135">Se o protocolo da URL for http, o Provedor de Internet será chamado por padrão.</span><span class="sxs-lookup"><span data-stu-id="90438-135">If the protocol for the URL is http, then the Internet Provider will be invoked by default.</span></span> <span data-ttu-id="90438-136">Se a URL apontar para um nó que contenha um script executável (tal como uma página .ASP), um **Record** que contém a fonte, em vez do conteúdo executado, será aberto por padrão.</span><span class="sxs-lookup"><span data-stu-id="90438-136">If the URL points to a node that contains an executable script (such as an .ASP page), then a **Record** containing the source rather than the executed contents is opened by default.</span></span> <span data-ttu-id="90438-137">Use o argumento *Options* para modificar esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="90438-137">Use the *Options* argument to modify this behavior.</span></span>

  - <span data-ttu-id="90438-p109">Um objeto **Record**. Um objeto **Record** aberto a partir de outro **Record** clonará o objeto **Record** original.</span><span class="sxs-lookup"><span data-stu-id="90438-p109">A **Record** object. A **Record** object opened from another **Record** will clone the original **Record** object.</span></span>

  - <span data-ttu-id="90438-p110">Um objeto **Command**. O objeto **Record** aberto representa a única linha retornada pela execução de **Command**. Se os resultados contiverem mais de uma única linha, o conteúdo da primeira linha será colocado no registro e um erro poderá ser adicionado à coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="90438-p110">A **Command** object. The opened **Record** object represents the single row returned by executing the **Command**. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="90438-p111">Uma instrução SQL SELECT. O objeto **Record** aberto representa a única linha retornada pela execução do conteúdo da sequência. Se os resultados contiverem mais de uma única linha, o conteúdo da primeira linha será colocado no registro e um erro poderá ser adicionado à coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="90438-p111">A SQL SELECT statement. The opened **Record** object represents the single row returned by executing the contents of the string. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="90438-146">O nome de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="90438-146">A table name.</span></span>

<span data-ttu-id="90438-147">Se o objeto **Record** representar uma entidade que não pode ser acessada com uma URL (por exemplo, uma linha de um **Recordset** derivada de um banco de dados), os valores da propriedade [ParentURL](parenturl-property-ado.md) e do campo acessado com a constante **adRecordURL** serão nulos.</span><span class="sxs-lookup"><span data-stu-id="90438-147">If the **Record** object represents an entity that cannot be accessed with a URL (for example, a row of a **Recordset** derived from a database), then the values of both the [ParentURL](parenturl-property-ado.md) property and the field accessed with the **adRecordURL** constant are null.</span></span>


> [!NOTE]
> <P><span data-ttu-id="90438-p112">[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs Absolutas e Relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="90438-p112">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


