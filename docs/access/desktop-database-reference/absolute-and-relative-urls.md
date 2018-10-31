---
title: URLs absolutas e relativas
TOCTitle: Absolute and relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: e5ac9c60be702841a4e45628ba609bdc63e14477
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862132"
---
# <a name="absolute-and-relative-urls"></a><span data-ttu-id="41984-102">URLs absolutas e relativas</span><span class="sxs-lookup"><span data-stu-id="41984-102">Absolute and relative URLs</span></span>

<span data-ttu-id="41984-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="41984-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="41984-104">A URL especifica o local de um destino armazenado em um computador local ou em rede, como um arquivo, um diretório, uma página HTML, uma imagem, um programa etc.</span><span class="sxs-lookup"><span data-stu-id="41984-104">A URL specifies the location of a target stored on a local or networked computer, such as a file, directory, HTML page, image, program, and so on.</span></span> <span data-ttu-id="41984-105">Nesta discussão, uma *URL absoluta* de tem este formato:</span><span class="sxs-lookup"><span data-stu-id="41984-105">In this discussion, an *absolute URL* is of the form:</span></span>

<span data-ttu-id="41984-106">*scheme://server/path/resource*</span><span class="sxs-lookup"><span data-stu-id="41984-106">*scheme://server/path/resource*</span></span>

<span data-ttu-id="41984-107">onde:</span><span class="sxs-lookup"><span data-stu-id="41984-107">where:</span></span>

|<span data-ttu-id="41984-108">Nome</span><span class="sxs-lookup"><span data-stu-id="41984-108">Name</span></span> |<span data-ttu-id="41984-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="41984-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="41984-110">*scheme*</span><span class="sxs-lookup"><span data-stu-id="41984-110">*scheme*</span></span>|<span data-ttu-id="41984-111">Especifica como o *recurso* deve ser acessado.</span><span class="sxs-lookup"><span data-stu-id="41984-111">Specifies how the *resource* is to be accessed.</span></span>|
|<span data-ttu-id="41984-112">*server*</span><span class="sxs-lookup"><span data-stu-id="41984-112">*server*</span></span>|<span data-ttu-id="41984-113">Especifica o nome do computador onde o *recurso* está localizado.</span><span class="sxs-lookup"><span data-stu-id="41984-113">Specifies the name of the computer where the *resource* is located.</span></span>|
|<span data-ttu-id="41984-114">*path*</span><span class="sxs-lookup"><span data-stu-id="41984-114">*path*</span></span>|<span data-ttu-id="41984-p102">Especifica a sequência de diretórios que levam ao destino. Se *resource* estiver omitido, o destino será o último diretório de *path*.</span><span class="sxs-lookup"><span data-stu-id="41984-p102">Specifies the sequence of directories leading to the target. If *resource* is omitted, the target is the last directory in *path*.</span></span>|
|<span data-ttu-id="41984-117">*resource*</span><span class="sxs-lookup"><span data-stu-id="41984-117">*resource*</span></span>|<span data-ttu-id="41984-118">Se for incluído, o *recurso* é o destino e é normalmente o nome de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="41984-118">If included, *resource* is the target, and is typically the name of a file.</span></span> <span data-ttu-id="41984-119">Talvez seja um *arquivo simples*, contendo um único fluxo binário de bytes ou um *documento estruturado*, contendo um ou mais armazenamentos e fluxos binários de bytes.</span><span class="sxs-lookup"><span data-stu-id="41984-119">It may be a *simple file*, containing a single binary stream of bytes, or a *structured document*, containing one or more storages and binary streams of bytes.</span></span>|

<span data-ttu-id="41984-120">Uma *URL absoluta* contém todas as informações necessárias para localizar um recurso.</span><span class="sxs-lookup"><span data-stu-id="41984-120">An *absolute URL* contains all the information necessary to locate a resource.</span></span>

<span data-ttu-id="41984-p104">A *URL relativa* localiza um recurso usando uma URL absoluta como ponto inicial. Na verdade, a "URL completa" do destino é especificada concatenando as URLs absoluta e relativa. Em geral, uma URL relativa consiste apenas no  *path* e, opcionalmente, no *resource*, mas não no *scheme* ou no *server*.</span><span class="sxs-lookup"><span data-stu-id="41984-p104">A *relative URL* locates a resource using an absolute URL as a starting point. In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs. A relative URL typically consists only of the *path*, and optionally, the *resource*, but no *scheme* or *server*.</span></span>

## <a name="url-scheme-registration"></a><span data-ttu-id="41984-124">Registro do esquema URL</span><span class="sxs-lookup"><span data-stu-id="41984-124">URL scheme registration</span></span>

<span data-ttu-id="41984-125">Se um provedor oferece suporte a URLs, ele irá registrar para um ou mais esquemas de URL.</span><span class="sxs-lookup"><span data-stu-id="41984-125">If a provider supports URLs, it will register for one or more URL schemes.</span></span> <span data-ttu-id="41984-126">Isso significa que nenhum URL usando esse esquema automaticamente invocará o provedor registrado.</span><span class="sxs-lookup"><span data-stu-id="41984-126">This means that any URLs using this scheme will automatically invoke the registered provider.</span></span> <span data-ttu-id="41984-127">Por exemplo, o esquema *http* está registrado para o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="41984-127">For example, the *http* scheme is registered to the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="41984-128">ADO pressupõe que todas as URLs prefixadas com "http" representam pastas da web ou arquivos a ser usado com o Internet Publishing Provider.</span><span class="sxs-lookup"><span data-stu-id="41984-128">ADO assumes all URLs prefixed with "http" represent web folders or files to be used with the Internet Publishing Provider.</span></span> <span data-ttu-id="41984-129">Para obter informações sobre os esquemas registrados pelo seu provedor, consulte a documentação do provedor.</span><span class="sxs-lookup"><span data-stu-id="41984-129">For information about the schemes registered by your provider, see your provider documentation.</span></span>

## <a name="defining-context-with-a-url"></a><span data-ttu-id="41984-130">Definindo o contexto com uma URL</span><span class="sxs-lookup"><span data-stu-id="41984-130">Defining context with a URL</span></span>

<span data-ttu-id="41984-p106">Uma das funções de uma conexão aberta, representada por um objeto [Connection](connection-object-ado.md), é restringir as operações subsequentes à fonte de dados representada por essa conexão, ou seja, a conexão define o contexto das operações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="41984-p106">One function of an open connection, represented by a [Connection](connection-object-ado.md) object, is to restrict subsequent operations to the data source represented by that connection. That is, the connection defines the context for subsequent operations.</span></span>

<span data-ttu-id="41984-p107">Com o ADO 2.5, uma URL absoluta também pode definir um contexto. Por exemplo, quando um objeto [Record](record-object-ado.md) é aberto com uma URL absoluta, um objeto **Connection** é implicitamente criado para representar o recurso especificado pela URL.</span><span class="sxs-lookup"><span data-stu-id="41984-p107">With ADO 2.5, an absolute URL may also define a context. For example, when a [Record](record-object-ado.md) object is opened with an absolute URL, a **Connection** object is implicitly created to represent the resource specified by the URL.</span></span>

<span data-ttu-id="41984-135">Uma URL absoluta que define um contexto pode ser especificada no parâmetro *ActiveConnection* do objeto **Record** do método [Open](open-method-ado-record.md) .</span><span class="sxs-lookup"><span data-stu-id="41984-135">An absolute URL that defines a context may be specified in the *ActiveConnection* parameter of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="41984-136">Uma URL absoluta também pode ser especificada como o valor da nova `URL=` palavra-chave em *ActiveConnection* do método [Open](open-method-ado-recordset.md) do objeto [Recordset](recordset-object-ado.md) e o parâmetro de *ConnectionString* método [Open](open-method-ado-connection.md) do objeto **Conexão** Use o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="41984-136">An absolute URL may also be specified as the value of the new `URL=` keyword in the **Connection** object [Open](open-method-ado-connection.md) method *ConnectionString* parameter, and the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method *ActiveConnection* parameter.</span></span>

<span data-ttu-id="41984-137">O contexto também pode ser definido com um objeto **Record** ou **Recordset** aberto que representa um diretório, pois esses objetos já possuem um objeto **Connection** implicitamente ou explicitamente declarado que especifica o contexto.</span><span class="sxs-lookup"><span data-stu-id="41984-137">Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.</span></span>

## <a name="scoped-operations"></a><span data-ttu-id="41984-138">Operações delimitadas</span><span class="sxs-lookup"><span data-stu-id="41984-138">Scoped operations</span></span>

<span data-ttu-id="41984-139">O contexto simultaneamente define um *escopo*— ou seja, o diretório e seus subdiretórios que podem participar das operações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="41984-139">The context simultaneously defines a *scope*—that is, the directory and its subdirectories that may participate in subsequent operations.</span></span> <span data-ttu-id="41984-140">O objeto **Record** possui vários métodos de escoopo, incluindo o [CopyRecord](copyrecord-method-ado.md), o [MoveRecord](moverecord-method-ado.md) e o [DeleteRecord](deleterecord-method-ado.md), que operam em um diretório e em todos os seus respectivos subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="41984-140">The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](deleterecord-method-ado.md), that operate on a directory and all its subdirectories.</span></span>

## <a name="relative-urls-as-command-text"></a><span data-ttu-id="41984-141">URLs relativas como texto de comando</span><span class="sxs-lookup"><span data-stu-id="41984-141">Relative URLs as command text</span></span>

<span data-ttu-id="41984-142">Uma cadeia de caracteres especificando um comando a ser executado na fonte de dados pode ser especificada no parâmetro de *CommandText* do método **Execute** do **Conexão** objeto e o parâmetro de *origem* método **Open** do objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="41984-142">A string specifying a command to be executed on the data source may be specified in the **Connection** object **Execute** method *CommandText* parameter, and the **Recordset** object **Open** method *Source* parameter.</span></span>

<span data-ttu-id="41984-143">Uma URL relativa pode ser especificada no parâmetro *CommandText* ou *fonte* .</span><span class="sxs-lookup"><span data-stu-id="41984-143">A relative URL may be specified in the *CommandText* or *Source* parameter.</span></span> <span data-ttu-id="41984-144">Na verdade, a URL relativa não especifica um comando (por exemplo, um comando SQL); ela é simplesmente especificada nesses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="41984-144">The relative URL does not actually specify a command (such as an SQL command); it is merely specified in those parameters.</span></span> <span data-ttu-id="41984-145">Além disso, o contexto da conexão ativa deve ser uma URL absoluta e o parâmetro de *opção* deve ser definido como **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="41984-145">In addition, the context of the active connection must be an absolute URL, and the *Option* parameter must be set to **adCmdTableDirect**.</span></span>

<span data-ttu-id="41984-146">Por exemplo, um **Recordset** poderia ser aberto no arquivo Readme25.txt do diretório Winnt/system32 da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="41984-146">For example, a **Recordset** could be opened on the Readme25.txt file of the Winnt/system32 directory like this:</span></span>

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<span data-ttu-id="41984-147">A URL absoluta na sequência de conexão Especifica o servidor (YourServer) e o caminho (Winnt).</span><span class="sxs-lookup"><span data-stu-id="41984-147">The absolute URL in the connection string specifies the server (YourServer) and the path (Winnt).</span></span> <span data-ttu-id="41984-148">Essa URL também define o contexto.</span><span class="sxs-lookup"><span data-stu-id="41984-148">This URL also defines the context.</span></span>

<span data-ttu-id="41984-149">A URL relativa no texto de comando usa a URL absoluta como ponto de partida e especifica o restante do caminho (system32) e o arquivo seja aberto (Readme25.txt).</span><span class="sxs-lookup"><span data-stu-id="41984-149">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (system32) and the file to open (Readme25.txt).</span></span>

<span data-ttu-id="41984-150">O campo de opções indica que o tipo de comando é uma URL relativa.</span><span class="sxs-lookup"><span data-stu-id="41984-150">The options field indicates that the command type is a relative URL.</span></span>

<span data-ttu-id="41984-151">Em outro exemplo, o código a seguir abrirá um **Recordset** no conteúdo do diretório:</span><span class="sxs-lookup"><span data-stu-id="41984-151">As another example, the following code will open a **Recordset** on the contents of the directory:</span></span>

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a><span data-ttu-id="41984-152">Esquemas URL fornecidos pelo provedor de OLE DB</span><span class="sxs-lookup"><span data-stu-id="41984-152">OLE DB provider-supplied URL schemes</span></span>

<span data-ttu-id="41984-153">A parte principal de uma URL totalmente qualificada é o *esquema* usado para acessar o recurso identificado pelo restante da URL.</span><span class="sxs-lookup"><span data-stu-id="41984-153">The leading part of a fully-qualified URL is the *scheme* used to access the resource identified by the remainder of the URL.</span></span> <span data-ttu-id="41984-154">Exemplos são HTTP (HyperText Transfer Protocol) e FTP (File Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="41984-154">Examples are HTTP (HyperText Transfer Protocol) and FTP (File Transfer Protocol).</span></span>

<span data-ttu-id="41984-155">O ADO oferece suporte aos provedores OLE DB que reconhecem seus próprios esquemas URL.</span><span class="sxs-lookup"><span data-stu-id="41984-155">ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="41984-156">Por exemplo, o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), quais acessos "publicado" arquivos do Windows 2000, reconhece o esquema HTTP existente.</span><span class="sxs-lookup"><span data-stu-id="41984-156">For example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</span></span>


