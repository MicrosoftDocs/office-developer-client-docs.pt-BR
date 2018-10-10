---
title: URLs absolutas e relativas
TOCTitle: Absolute and Relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc0cb3086f8fdfa032c005f7e2d219dab56999b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464723"
---
# <a name="absolute-and-relative-urls"></a><span data-ttu-id="0d0f7-102">URLs absolutas e relativas</span><span class="sxs-lookup"><span data-stu-id="0d0f7-102">Absolute and Relative URLs</span></span>

<span data-ttu-id="0d0f7-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d0f7-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="0d0f7-104">Uma URL especifica o local de um destino armazenado em um computador local ou em rede, como um arquivo, diretório, página HTML, imagem, programa e assim por diante *.*</span><span class="sxs-lookup"><span data-stu-id="0d0f7-104">A URL specifies the location of a target stored on a local or networked computer, such as a file, directory, HTML page, image, program, and so on *.*</span></span> <span data-ttu-id="0d0f7-105">Nesta discussão, uma *URL absoluta* de tem este formato:</span><span class="sxs-lookup"><span data-stu-id="0d0f7-105">In this discussion, an *absolute URL* is of the form:</span></span>

<span data-ttu-id="0d0f7-106">*scheme://server/path/resource*</span><span class="sxs-lookup"><span data-stu-id="0d0f7-106">*scheme://server/path/resource*</span></span>

<span data-ttu-id="0d0f7-107">onde:</span><span class="sxs-lookup"><span data-stu-id="0d0f7-107">where:</span></span>

  - <span data-ttu-id="0d0f7-108">*scheme*</span><span class="sxs-lookup"><span data-stu-id="0d0f7-108">*scheme*</span></span>

  - <span data-ttu-id="0d0f7-109">Especifica como o *recurso* deve ser acessado.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-109">Specifies how the *resource* is to be accessed.</span></span>

  - <span data-ttu-id="0d0f7-110">*server*</span><span class="sxs-lookup"><span data-stu-id="0d0f7-110">*server*</span></span>

  - <span data-ttu-id="0d0f7-111">Especifica o nome do computador onde o *recurso* está localizado.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-111">Specifies the name of the computer where the *resource* is located.</span></span>

  - <span data-ttu-id="0d0f7-112">*path*</span><span class="sxs-lookup"><span data-stu-id="0d0f7-112">*path*</span></span>

  - <span data-ttu-id="0d0f7-p102">Especifica a sequência de diretórios que levam ao destino. Se *resource* estiver omitido, o destino será o último diretório de *path*.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-p102">Specifies the sequence of directories leading to the target. If *resource* is omitted, the target is the last directory in *path*.</span></span>

  - <span data-ttu-id="0d0f7-115">*resource*</span><span class="sxs-lookup"><span data-stu-id="0d0f7-115">*resource*</span></span>

  - <span data-ttu-id="0d0f7-116">Se for incluído, o *recurso* é o destino e é normalmente o nome de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-116">If included, *resource* is the target, and is typically the name of a file.</span></span> <span data-ttu-id="0d0f7-117">Talvez seja um *arquivo simples,* contendo um único fluxo binário de bytes ou um *documento estruturado,* contendo um ou mais armazenamentos e fluxos binários de bytes.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-117">It may be a *simple file,* containing a single binary stream of bytes, or a *structured document,* containing one or more storages and binary streams of bytes.</span></span>

<span data-ttu-id="0d0f7-118">Uma *URL absoluta* contém todas as informações necessárias para localizar um recurso.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-118">An *absolute URL* contains all the information necessary to locate a resource.</span></span>

<span data-ttu-id="0d0f7-p104">A *URL relativa* localiza um recurso usando uma URL absoluta como ponto inicial. Na verdade, a "URL completa" do destino é especificada concatenando as URLs absoluta e relativa. Em geral, uma URL relativa consiste apenas no  *path* e, opcionalmente, no *resource*, mas não no *scheme* ou no *server*.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-p104">A *relative URL* locates a resource using an absolute URL as a starting point. In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs. A relative URL typically consists only of the *path*, and optionally, the *resource*, but no *scheme* or *server*.</span></span>

## <a name="url-scheme-registration"></a><span data-ttu-id="0d0f7-122">Registro do esquema URL</span><span class="sxs-lookup"><span data-stu-id="0d0f7-122">URL Scheme Registration</span></span>

<span data-ttu-id="0d0f7-123">Se um provedor oferece suporte a URLs, ele irá registrar para um ou mais esquemas de URL.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-123">If a provider supports URLs, it will register for one or more URL schemes.</span></span> <span data-ttu-id="0d0f7-124">Isso significa que nenhum URL usando esse esquema automaticamente invocará o provedor registrado.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-124">This means that any URLs using this scheme will automatically invoke the registered provider.</span></span> <span data-ttu-id="0d0f7-125">Por exemplo, o esquema *http* está registrado para o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="0d0f7-125">For example, the *http* scheme is registered to the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="0d0f7-126">ADO pressupõe que todas as URLs prefixadas com "http" representam pastas da Web ou arquivos a ser usado com o Internet Publishing Provider.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-126">ADO assumes all URLs prefixed with "http" represent Web folders or files to be used with the Internet Publishing Provider.</span></span> <span data-ttu-id="0d0f7-127">Para obter informações sobre os esquemas registrados pelo seu provedor, consulte a documentação do provedor.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-127">For information about the schemes registered by your provider, see your provider documentation.</span></span>

## <a name="defining-context-with-a-url"></a><span data-ttu-id="0d0f7-128">Definindo o contexto com uma URL</span><span class="sxs-lookup"><span data-stu-id="0d0f7-128">Defining Context with a URL</span></span>

<span data-ttu-id="0d0f7-p106">Uma das funções de uma conexão aberta, representada por um objeto [Connection](connection-object-ado.md), é restringir as operações subsequentes à fonte de dados representada por essa conexão, ou seja, a conexão define o contexto das operações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-p106">One function of an open connection, represented by a [Connection](connection-object-ado.md) object, is to restrict subsequent operations to the data source represented by that connection. That is, the connection defines the context for subsequent operations.</span></span>

<span data-ttu-id="0d0f7-p107">Com o ADO 2.5, uma URL absoluta também pode definir um contexto. Por exemplo, quando um objeto [Record](record-object-ado.md) é aberto com uma URL absoluta, um objeto **Connection** é implicitamente criado para representar o recurso especificado pela URL.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-p107">With ADO 2.5, an absolute URL may also define a context. For example, when a [Record](record-object-ado.md) object is opened with an absolute URL, a **Connection** object is implicitly created to represent the resource specified by the URL.</span></span>

<span data-ttu-id="0d0f7-133">Uma URL absoluta que define um contexto pode ser especificada no parâmetro *ActiveConnection* do objeto **Record** do método [Open](open-method-ado-record.md) .</span><span class="sxs-lookup"><span data-stu-id="0d0f7-133">An absolute URL that defines a context may be specified in the *ActiveConnection* parameter of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="0d0f7-134">Uma URL absoluta também pode ser especificada como o valor da nova "URL**=**" palavra-chave em \*ActiveConnection do método [Open](open-method-ado-recordset.md) do objeto [Recordset](recordset-object-ado.md) e o parâmetro de *ConnectionString* método [Open](open-method-ado-connection.md) do objeto **Conexão** \*parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-134">An absolute URL may also be specified as the value of the new "URL**=**" keyword in the **Connection** object [Open](open-method-ado-connection.md) method *ConnectionString* parameter, and the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method *ActiveConnection* parameter.</span></span>

<span data-ttu-id="0d0f7-135">O contexto também pode ser definido com um objeto **Record** ou **Recordset** aberto que representa um diretório, pois esses objetos já possuem um objeto **Connection** implicitamente ou explicitamente declarado que especifica o contexto.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-135">Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.</span></span>

## <a name="scoped-operations"></a><span data-ttu-id="0d0f7-136">Operações delimitadas</span><span class="sxs-lookup"><span data-stu-id="0d0f7-136">Scoped Operations</span></span>

<span data-ttu-id="0d0f7-137">O contexto simultaneamente define um *escopo* — ou seja, o diretório e seus subdiretórios que podem participar das operações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-137">The context simultaneously defines a *scope* — that is, the directory and its subdirectories that may participate in subsequent operations.</span></span> <span data-ttu-id="0d0f7-138">O objeto **Record** possui vários métodos de escoopo, incluindo o [CopyRecord](copyrecord-method-ado.md), o [MoveRecord](moverecord-method-ado.md) e o [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), que operam em um diretório e em todos os seus respectivos subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-138">The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), that operate on a directory and all its subdirectories.</span></span>

## <a name="relative-urls-as-command-text"></a><span data-ttu-id="0d0f7-139">URLs relativas como texto de comando</span><span class="sxs-lookup"><span data-stu-id="0d0f7-139">Relative URLs as Command Text</span></span>

<span data-ttu-id="0d0f7-140">Uma cadeia de caracteres especificando um comando a ser executado na fonte de dados pode ser especificada no parâmetro de *CommandText* do método **Execute** do **Conexão** objeto e o parâmetro de *origem* método **Open** do objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="0d0f7-140">A string specifying a command to be executed on the data source may be specified in the **Connection** object **Execute** method *CommandText* parameter, and the **Recordset** object **Open** method *Source* parameter.</span></span>

<span data-ttu-id="0d0f7-141">Uma URL relativa pode ser especificada no parâmetro *CommandText* ou *fonte* .</span><span class="sxs-lookup"><span data-stu-id="0d0f7-141">A relative URL may be specified in the *CommandText* or *Source* parameter.</span></span> <span data-ttu-id="0d0f7-142">Na verdade, a URL relativa não especifica um comando (por exemplo, um comando SQL); ela é simplesmente especificada nesses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-142">The relative URL does not actually specify a command (such as an SQL command); it is merely specified in those parameters.</span></span> <span data-ttu-id="0d0f7-143">Além disso, o contexto da conexão ativa deve ser uma URL absoluta e o parâmetro de *opção* deve ser definido como **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-143">In addition, the context of the active connection must be an absolute URL, and the *Option* parameter must be set to **adCmdTableDirect**.</span></span>

<span data-ttu-id="0d0f7-144">Por exemplo, um **Recordset** poderia ser aberto no arquivo Readme25.txt do diretório Winnt/system32 da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0d0f7-144">For example, a **Recordset** could be opened on the Readme25.txt file of the Winnt/system32 directory like this:</span></span>

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<span data-ttu-id="0d0f7-145">A URL absoluta na sequência de conexão Especifica o servidor (YourServer) e a (' caminho) e o caminho (Winnt).</span><span class="sxs-lookup"><span data-stu-id="0d0f7-145">The absolute URL in the connection string specifies the server (YourServer ) and the path () and the path (Winnt ).</span></span> <span data-ttu-id="0d0f7-146">Essa URL também define o contexto.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-146">This URL also defines the context.</span></span>

<span data-ttu-id="0d0f7-147">A URL relativa no texto de comando usa a URL absoluta como ponto de partida e especifica o restante do caminho (system32) e o arquivo seja aberto () e o arquivo seja aberto (Readme25.txt).</span><span class="sxs-lookup"><span data-stu-id="0d0f7-147">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (system32 ) and the file to open () and the file to open (Readme25.txt ).</span></span>

<span data-ttu-id="0d0f7-148">O campo de opções () indica que o tipo de comando é uma URL relativa.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-148">The options field () indicates that the command type is a relative URL.</span></span>

<span data-ttu-id="0d0f7-149">Em outro exemplo, o código a seguir abrirá um **Recordset** no conteúdo do diretório:</span><span class="sxs-lookup"><span data-stu-id="0d0f7-149">As another example, the following code will open a **Recordset** on the contents of the directory:</span></span>

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a><span data-ttu-id="0d0f7-150">Esquemas URL fornecidos pelo OLE DB Provider</span><span class="sxs-lookup"><span data-stu-id="0d0f7-150">OLE DB Provider-Supplied URL Schemes</span></span>

<span data-ttu-id="0d0f7-151">A parte principal de uma URL totalmente qualificada é o *esquema* usado para acessar o recurso identificado pelo restante da URL.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-151">The leading part of a fully-qualified URL is the *scheme* used to access the resource identified by the remainder of the URL.</span></span> <span data-ttu-id="0d0f7-152">Exemplos são HTTP (HyperText Transfer Protocol) e FTP (File Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="0d0f7-152">Examples are HTTP (HyperText Transfer Protocol) and FTP (File Transfer Protocol).</span></span>

<span data-ttu-id="0d0f7-p113">O ADO oferece suporte aos provedores OLE DB que reconhecem seus próprios esquemas URL. Por exemplo, o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* que acessa arquivos "publicados" do Windows 2000, reconhece o esquema HTTP existente.</span><span class="sxs-lookup"><span data-stu-id="0d0f7-p113">ADO supports OLE DB providers that recognize their own URL schemes. For example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</span></span>

