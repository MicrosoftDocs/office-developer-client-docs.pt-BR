---
title: What's new in ActiveX Data Objects (ADO)
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 232af159c669968c9c3b4d3d65acbc181f958689
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998900"
---
# <a name="whats-new-in-ado"></a><span data-ttu-id="93ea5-102">Novidades do ADO</span><span class="sxs-lookup"><span data-stu-id="93ea5-102">What's new in ADO</span></span>

<span data-ttu-id="93ea5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="93ea5-103">**Applies to**: Access 2013, Office 2013</span></span> 
 
<span data-ttu-id="93ea5-p101">Os novos recursos a seguir e a documentação aperfeiçoada foram incluídos no ADO versão 2.5. A lista abrange o ADO, o ADO MD e o ADOX.</span><span class="sxs-lookup"><span data-stu-id="93ea5-p101">The following new features and enhanced documentation are included in the ADO 2.5 release. This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="93ea5-106">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="93ea5-106">New features</span></span>

- <span data-ttu-id="93ea5-107">**[Records e streams](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="93ea5-107">**[Records and streams](chapter-10-records-and-streams.md)**</span></span>

  <span data-ttu-id="93ea5-108">Esta versão do ADO introduz o objeto [Record](record-object-ado.md) , que pode representar e gerenciar coisas como diretórios e arquivos em um sistema de arquivos e pastas e mensagens em um sistema de email.</span><span class="sxs-lookup"><span data-stu-id="93ea5-108">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an email system.</span></span> <span data-ttu-id="93ea5-109">Um **Record** também pode representar uma linha em um [Recordset](recordset-object-ado.md), embora os objetos **Record** e **Recordset** tenham métodos e propriedades diferentes.</span><span class="sxs-lookup"><span data-stu-id="93ea5-109">A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

  <span data-ttu-id="93ea5-110">O novo objeto [Stream](stream-object-ado.md) permite ler, gravar e gerenciar o fluxo binário de bytes ou o texto que abrange um fluxo de arquivo ou de mensagem.</span><span class="sxs-lookup"><span data-stu-id="93ea5-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

- <span data-ttu-id="93ea5-111">**[Uso da URL](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="93ea5-111">**[URL usage](absolute-and-relative-urls.md)**</span></span>

  <span data-ttu-id="93ea5-p103">Esta versão também introduz o uso de URLs, uma alternativa para sequências de conexão e texto de comando, para nomear objetos de repositório de dados. As URLs podem ser usadas com os objetos [Connection](connection-object-ado.md) e **Recordset** existentes, e também com os novos objetos **Record** e **Stream**.</span><span class="sxs-lookup"><span data-stu-id="93ea5-p103">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects. URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

  <span data-ttu-id="93ea5-p104">Com esta versão, o ADO oferece suporte a provedores OLE DB que reconhecem seus próprios esquemas URL. Por exemplo, o [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* que acessa o sistema de arquivos do Windows 2000, reconhece o esquema HTTP existente.</span><span class="sxs-lookup"><span data-stu-id="93ea5-p104">With this release, ADO supports OLE DB providers that recognize their own URL schemes. For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

- <span data-ttu-id="93ea5-116">**[Campos especiais para provedores de fontes do documento](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="93ea5-116">**[Special fields for document source providers](records-and-provider-supplied-fields.md)**</span></span>

  <span data-ttu-id="93ea5-117">Uma classe especial de provedores, chamado provedores de *documento de origem* , gerenciar pastas e documentos.</span><span class="sxs-lookup"><span data-stu-id="93ea5-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="93ea5-118">Quando um objeto **Record** representa um documento, ou um objeto **Recordset** representa uma pasta de documentos, o provedor de fonte de documentos preenche esses objetos com um conjunto exclusivo de campos que descrevem as características do documento.</span><span class="sxs-lookup"><span data-stu-id="93ea5-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="93ea5-119">Esses campos constituem um *recurso* de **registro** ou **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="93ea5-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="93ea5-120">Novos tópicos de referência</span><span class="sxs-lookup"><span data-stu-id="93ea5-120">New reference topics</span></span>

### <a name="properties"></a><span data-ttu-id="93ea5-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93ea5-121">Properties</span></span>

<span data-ttu-id="93ea5-122">As novas propriedades a seguir foram incluídas nesta versão.</span><span class="sxs-lookup"><span data-stu-id="93ea5-122">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93ea5-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="93ea5-123">Property</span></span></p></th>
<th><p><span data-ttu-id="93ea5-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="93ea5-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-125"><a href="charset-property-ado.md">Charset</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-125"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-126">Indica o conjunto de caracteres no qual o conteúdo de um objeto <strong>Stream</strong> de texto deve ser convertido.</span><span class="sxs-lookup"><span data-stu-id="93ea5-126">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-127"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-127"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-128">Indica se a posição atual está no final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="93ea5-128">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-130">Indica o caractere binário a ser usado como o separador de linha nos objetos <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="93ea5-130">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-131"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-131"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-132">Indica as permissões disponíveis para modificar os dados em um objeto <strong>Connection</strong>, <strong>Record</strong> ou <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="93ea5-132">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-133"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-133"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-134">Indica uma sequência de URL absoluta que aponta para o <strong>Record</strong> pai do objeto <strong>Record</strong> atual.</span><span class="sxs-lookup"><span data-stu-id="93ea5-134">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-135"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-135"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-136">Indica a posição atual em um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="93ea5-136">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-137"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-137"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-138">Indica o tipo de objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="93ea5-138">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-139"><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Tamanho</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-139"><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Size</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-140">Indica o tamanho do fluxo em número de bytes.</span><span class="sxs-lookup"><span data-stu-id="93ea5-140">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-141"><a href="source-property-ado-record.md">Origem</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-141"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-142">Indica a entidade representada pelo objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="93ea5-142">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-143"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-143"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-144">Indica todos os objetos aplicáveis, independentemente de seu estado: aberto ou fechado.</span><span class="sxs-lookup"><span data-stu-id="93ea5-144">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="93ea5-145">Indica todos os objetos aplicáveis que executam um método assíncrono, independentemente de seu estado atual: conexão, execução ou recuperação.</span><span class="sxs-lookup"><span data-stu-id="93ea5-145">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-146"><a href="type-property-ado-stream.md">Tipo</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-146"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-147">Indica o tipo de dados contido no objeto <strong>Stream</strong> (binário ou de texto).</span><span class="sxs-lookup"><span data-stu-id="93ea5-147">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a><span data-ttu-id="93ea5-148">Métodos</span><span class="sxs-lookup"><span data-stu-id="93ea5-148">Methods</span></span>

<span data-ttu-id="93ea5-149">Os novos métodos a seguir foram incluídos nesta versão.</span><span class="sxs-lookup"><span data-stu-id="93ea5-149">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93ea5-150">Método</span><span class="sxs-lookup"><span data-stu-id="93ea5-150">Method</span></span></p></th>
<th><p><span data-ttu-id="93ea5-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="93ea5-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-153">Copia um arquivo ou um diretório, e seu conteúdo, para outro local.</span><span class="sxs-lookup"><span data-stu-id="93ea5-153">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-154"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-154"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-155">Copia o número especificado de caracteres ou bytes (dependendo do <strong>tipo</strong>) no <strong>objeto</strong> <strong>Stream</strong> para outro objeto <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="93ea5-155">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-156"><a href="deleterecord-method-ado.md">ExcluirRegistro</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-157">Exclui um arquivo ou um diretório e todos os respectivos subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="93ea5-157">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-158"><a href="flush-method-ado.md">Liberar</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-158"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-159">Força o conteúdo do objeto <strong>Stream</strong> restante no buffer do ADO para o objeto subjacente ao qual o objeto <strong>Stream</strong> está associado.</span><span class="sxs-lookup"><span data-stu-id="93ea5-159">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-160"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-160"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-161">Retorna um <strong>Recordset</strong> cujas linhas representam os arquivos e os subdiretórios no diretório representado por este <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="93ea5-161">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-163">Carrega o conteúdo de um arquivo existente para um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="93ea5-163">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-164"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-164"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-165">Move um arquivo, ou um diretório e seu conteúdo, para outro local.</span><span class="sxs-lookup"><span data-stu-id="93ea5-165">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-166"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-166"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-167">Abre um objeto <strong>Record</strong> existente ou cria um novo arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="93ea5-167">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-168"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-168"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-169">Abre um objeto <strong>Stream</strong> para manipular fluxos de dados de texto ou binários.</span><span class="sxs-lookup"><span data-stu-id="93ea5-169">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-170"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-170"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-171">Lê um número de bytes especificado de um objeto <strong>Stream</strong> binário.</span><span class="sxs-lookup"><span data-stu-id="93ea5-171">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-172"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-172"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-173">Lê o número de caracteres especificado de um objeto <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="93ea5-173">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-174"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-174"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-175">Salva o conteúdo binário de um <strong>Stream</strong> para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="93ea5-175">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-176"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-176"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-177">Define a posição que é o final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="93ea5-177">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-178"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-178"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-179">Ignora uma linha inteira na leitura de um objeto <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="93ea5-179">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ea5-180"><a href="write-method-ado.md">Escrever</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-180"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-181">Grava dados binários em um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="93ea5-181">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ea5-182"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="93ea5-182"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="93ea5-183">Grava uma sequência de texto especificada em um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="93ea5-183">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="93ea5-184">Nova documentação aprimorada</span><span class="sxs-lookup"><span data-stu-id="93ea5-184">New and enhanced documentation</span></span>

- <span data-ttu-id="93ea5-185">**[Tópicos de exemplo de código](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="93ea5-185">**[Code example topics](ado-code-examples.md)**</span></span>

  <span data-ttu-id="93ea5-186">Os exemplos foram expandidos para conter os exemplos de código escritos em Microsoft Visual C++ e o Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="93ea5-186">The examples have been expanded to contain code examples written in Microsoft Visual C++ and Microsoft Visual J++.</span></span> <span data-ttu-id="93ea5-187">Você pode copiar e colar esses exemplos de código em seu editor.</span><span class="sxs-lookup"><span data-stu-id="93ea5-187">You can copy and paste these code examples into your editor.</span></span>

- <span data-ttu-id="93ea5-188">**[Tópicos de provedor](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="93ea5-188">**[Provider topics](appendix-a-providers.md)**</span></span>

  <span data-ttu-id="93ea5-189">Um novo tópico foi incluído e explica como usar o ADO com o [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="93ea5-189">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

- <span data-ttu-id="93ea5-190">**[Programando com o ADO](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="93ea5-190">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

  <span data-ttu-id="93ea5-191">Esta nova seção contém dicas e truques para o uso do ADO com diversas linguagens de programação.</span><span class="sxs-lookup"><span data-stu-id="93ea5-191">This new section contains tips and tricks for using ADO with various programming languages.</span></span> <span data-ttu-id="93ea5-192">Ele contém os índices de sintaxe existentes para as extensões do Visual C++ para ADO e ADO/WFC, bem como novas informações específicas para os desenvolvedores que usam o Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, ou Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="93ea5-192">It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, or Microsoft Visual J++.</span></span>

