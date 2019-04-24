---
title: Objeto Stream (ADO)
TOCTitle: Stream object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1f6d7e8f64f6b14ea699006fc0461cdf0ded2a06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308481"
---
# <a name="stream-object-ado"></a><span data-ttu-id="d6e67-102">Objeto Stream (ADO)</span><span class="sxs-lookup"><span data-stu-id="d6e67-102">Stream object (ADO)</span></span>


<span data-ttu-id="d6e67-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6e67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6e67-104">Representa um fluxo de dados ou texto binário.</span><span class="sxs-lookup"><span data-stu-id="d6e67-104">Represents a stream of binary data or text.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6e67-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6e67-105">Remarks</span></span>

<span data-ttu-id="d6e67-106">Em hierarquias estruturadas em árvore, como um sistema de arquivos ou um sistema de email, um [registro](record-object-ado.md) pode ter um fluxo binário padrão de bits associado a ele que contenha o conteúdo do arquivo ou o email.</span><span class="sxs-lookup"><span data-stu-id="d6e67-106">In tree-structured hierarchies such as a file system or an email system, a [Record](record-object-ado.md) may have a default binary stream of bits associated with it that contains the contents of the file or the email.</span></span> <span data-ttu-id="d6e67-107">Um objeto **Stream** pode ser usado para manipular campos ou registros que contenham esses fluxos de dados.</span><span class="sxs-lookup"><span data-stu-id="d6e67-107">A **Stream** object can be used to manipulate fields or records containing these streams of data.</span></span> <span data-ttu-id="d6e67-108">Um objeto **Stream** pode ser obtido dessas formas:</span><span class="sxs-lookup"><span data-stu-id="d6e67-108">A **Stream** object can be obtained in these ways:</span></span>

  - <span data-ttu-id="d6e67-p102">A partir de uma URL que aponta para um objeto (geralmente um arquivo) que contenha dados binários ou de texto. Esse objeto pode ser um documento simples, um objeto **Record** que representa um documento estruturado ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="d6e67-p102">From a URL pointing to an object (typically a file) containing binary or text data. This object can be a simple document, a **Record** object representing a structured document, or a folder.</span></span>

  - <span data-ttu-id="d6e67-p103">Pela abertura do objeto **Stream** padrão associado a um objeto **Record**. Obtenha o fluxo padrão associado ao objeto **Record**, quando **Record** estiver aberto, para eliminar um percurso circular apenas para abrir o fluxo.</span><span class="sxs-lookup"><span data-stu-id="d6e67-p103">By opening the default **Stream** object associated with a **Record** object. You can obtain the default stream associated with a **Record** object when the **Record** is opened, to eliminate a round-trip just to open the stream.</span></span>

  - <span data-ttu-id="d6e67-p104">Pelo instanciamento de um objeto **Stream**. Esses objetos **Stream** podem ser usados para armazenar dados no aplicativo. Ao contrário de um **Stream** associado a uma URL ou **Stream** padrão de um **Record**, um **Stream** instanciado não está associado a uma fonte base por padrão.</span><span class="sxs-lookup"><span data-stu-id="d6e67-p104">By instantiating a **Stream** object. These **Stream** objects can be used to store data for the purposes of your application. Unlike a **Stream** associated with a URL, or the default **Stream** of a **Record**, an instantiated **Stream** has no association with an underlying source by default.</span></span>

<span data-ttu-id="d6e67-116">Com os métodos e as propriedades e um objeto **Stream**, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d6e67-116">With the methods and properties of a **Stream** object, you can do the following:</span></span>

  - <span data-ttu-id="d6e67-117">Abrir um objeto **Stream** a partir de um **Record** ou uma URL com o método [Open](open-method-ado-stream.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-117">Open a **Stream** object from a **Record** or URL with the [Open](open-method-ado-stream.md) method.</span></span>

  - <span data-ttu-id="d6e67-118">Fechar um **Stream** com o método [Close](close-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-118">Close a **Stream** with the [Close](close-method-ado.md) method.</span></span>

  - <span data-ttu-id="d6e67-119">Inserir bytes ou texto para um **Stream** com os métodos [Write](write-method-ado.md) e [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-119">Input bytes or text to a **Stream** with the [Write](write-method-ado.md) and [WriteText](writetext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="d6e67-120">Ler os bytes do **Stream** com os métodos [Read](read-method-ado.md) e [ReadText](readtext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-120">Read bytes from the **Stream** with the [Read](read-method-ado.md) and [ReadText](readtext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="d6e67-121">Gravar quaisquer dados **Stream** que ainda estejam no buffer do ADO para o objeto base com o método [Flush](flush-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-121">Write any **Stream** data still in the ADO buffer to the underlying object with the [Flush](flush-method-ado.md) method.</span></span>

  - <span data-ttu-id="d6e67-122">Copiar os conteúdos de um **Stream** para outro **Stream** com o método [CopyTo](copyto-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-122">Copy the contents of a **Stream** to another **Stream** with the [CopyTo](copyto-method-ado.md) method.</span></span>

  - <span data-ttu-id="d6e67-123">Controlar quantas linhas serão lidas a partir do arquivo fonte com o método [SkipLine](skipline-method-ado.md) e a propriedade [LineSeparator](lineseparator-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-123">Control how lines are read from the source file with the [SkipLine](skipline-method-ado.md) method and the [LineSeparator](lineseparator-property-ado.md) property.</span></span>

  - <span data-ttu-id="d6e67-124">Determinar o final da posição do fluxo com a propriedade [EOS](eos-property-ado.md) e o método [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-124">Determine the end of stream position with the [EOS](eos-property-ado.md) property and [SetEOS](seteos-method-ado.md) method.</span></span>

  - <span data-ttu-id="d6e67-125">Salvar e restaurar os arquivos com os métodos [SaveToFile](savetofile-method-ado.md) e [LoadFromFile](loadfromfile-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-125">Save and restore data in files with the [SaveToFile](savetofile-method-ado.md) and [LoadFromFile](loadfromfile-method-ado.md) methods.</span></span>

  - <span data-ttu-id="d6e67-126">Especificar o conjunto de caracteres usados para repositório de **Stream** com a propriedade [Charset](charset-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-126">Specify the character set used for storing the **Stream** with the [Charset](charset-property-ado.md) property.</span></span>

  - <span data-ttu-id="d6e67-127">Interromper uma operação **Stream** assíncrona com o método [Cancel](cancel-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-127">Halt an asynchronous **Stream** operation with the [Cancel](cancel-method-ado.md) method.</span></span>

  - <span data-ttu-id="d6e67-128">Determinar o número de bytes em um **Stream** com a propriedade [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream).</span><span class="sxs-lookup"><span data-stu-id="d6e67-128">Determine the number of bytes in a **Stream** with the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) property.</span></span>

  - <span data-ttu-id="d6e67-129">Controlar a posição atual dentro de um **Stream** com a propriedade [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-129">Control the current position within a **Stream** with the [Position](position-property-ado.md) property.</span></span>

  - <span data-ttu-id="d6e67-130">Determinar o tipo de dados em um **Stream** com a propriedade [Type](type-property-ado-stream.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-130">Determine the type of data in a **Stream** with the [Type](type-property-ado-stream.md) property.</span></span>

  - <span data-ttu-id="d6e67-131">Determinar o estado atual do **Stream** (fechado, aberto ou executando) com a propriedade [State](state-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-131">Determine the current state of the **Stream** (closed, open, or executing) with the [State](state-property-ado.md) property.</span></span>

  - <span data-ttu-id="d6e67-132">Especificar o modo de acesso para o **Stream** com a propriedade [Mode](mode-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-132">Specify the access mode for the **Stream** with the [Mode](mode-property-ado.md) property.</span></span>

> [!NOTE]
> <span data-ttu-id="d6e67-133">[!OBSERVAçãO] As URLs que usam o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-133">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="d6e67-134">Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="d6e67-134">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


