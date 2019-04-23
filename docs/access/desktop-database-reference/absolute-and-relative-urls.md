---
title: URLs absolutas e relativas
TOCTitle: Absolute and relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a488617dc7ba0d7d1f7e38391f8382fa1e7ed247
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282098"
---
# <a name="absolute-and-relative-urls"></a>URLs absolutas e relativas

**Aplica-se ao:** Access 2013, Office 2013    

A URL especifica o local de um destino armazenado em um computador local ou em rede, como um arquivo, um diretório, uma página HTML, uma imagem, um programa etc. Nesta discussão, a *URL absoluta* terá este formato:

*scheme://server/path/resource*

onde:

|Nome |Descrição|
|:----|:----------|
|*scheme*|Especifica como o *resource* deve ser acessado.|
|*server*|Especifica o nome do computador que contém o *resource*.|
|*path*|Especifica a sequência de diretórios que levam ao destino. Se *resource* estiver omitido, o destino será o último diretório de *path*.|
|*recurso*|Se estiver incluído, *resource* será o destino e, geralmente, o nome de um arquivo. Pode ser um *arquivo simples*, contendo um único fluxo binário de bytes, ou um *documento estruturado*, contendo um ou mais armazenamentos e fluxos binários de bytes.|

A *URL absoluta* contém todas as informações necessárias à localização de um recurso.

A *URL relativa* localiza um recurso usando uma URL absoluta como ponto inicial. Na verdade, a "URL completa" do destino é especificada concatenando as URLs absoluta e relativa. Em geral, uma URL relativa consiste apenas no  *path* e, opcionalmente, no *resource*, mas não no *scheme* ou no *server*.

## <a name="url-scheme-registration"></a>Registro de esquema de URL

Se um provedor oferecer suporte a URLs, ele será registrado em um ou mais esquemas de URL. Isso significa que qualquer URL usando esse esquema invocará automaticamente o provedor registrado. Por exemplo, o esquema *http* é registrado no [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). O ADO assume que todas as URLs prefixadas com "http" representam pastas da Web ou arquivos a serem usados com o Internet Publishing Provider. Para obter informações sobre os esquemas registrados pelo seu provedor, consulte a documentação do provedor.

## <a name="defining-context-with-a-url"></a>Definindo contexto com uma URL

Uma das funções de uma conexão aberta, representada por um objeto [Connection](connection-object-ado.md), é restringir as operações subsequentes à fonte de dados representada por essa conexão, ou seja, a conexão define o contexto das operações subsequentes.

Com o ADO 2.5, uma URL absoluta também pode definir um contexto. Por exemplo, quando um objeto [Record](record-object-ado.md) é aberto com uma URL absoluta, um objeto **Connection** é implicitamente criado para representar o recurso especificado pela URL.

A URL absoluta que define um contexto pode ser especificada no parâmetro *ActiveConnection* do método [Open](open-method-ado-record.md) do objeto **Record**. `URL=` Uma URL absoluta também pode ser especificada como o valor da nova palavra-chave no parâmetro *ConnectionString* do método [Open](open-method-ado-connection.md) do objeto **Connection** e o objeto [Recordset](recordset-object-ado.md) [abrir](open-method-ado-recordset.md) método *ActiveConnection* Construtor.

O contexto também pode ser definido com um objeto **Record** ou **Recordset** aberto que representa um diretório, pois esses objetos já possuem um objeto **Connection** implicitamente ou explicitamente declarado que especifica o contexto.

## <a name="scoped-operations"></a>Operações com escopo

O contexto define simultaneamente um *escopo*, ou seja, o diretório e seus subdiretórios que podem participar de operações subsequentes. O objeto **Record** possui vários métodos de escoopo, incluindo o [CopyRecord](copyrecord-method-ado.md), o [MoveRecord](moverecord-method-ado.md) e o [DeleteRecord](deleterecord-method-ado.md), que operam em um diretório e em todos os seus respectivos subdiretórios.

## <a name="relative-urls-as-command-text"></a>URLs relativas como texto de comando

Uma sequência de caracteres que define um comando a ser executado na fonte de dados pode ser especificado no parâmetro *CommandText* do método **Execute** do objeto **Connection** e no parâmetro *Source* do método **Open** do objeto **Recordset**.

Uma URL relativa pode ser especificada no parâmetro *CommandText* ou *Source*. Na verdade, a URL relativa não especifica um comando (por exemplo, um comando SQL); ela é simplesmente especificada nesses parâmetros. O contexto da conexão ativa também deve ser uma URL absoluta, e o parâmetro *Option* deve ser definido como **adCmdTableDirect**.

Por exemplo, um **Recordset** poderia ser aberto no arquivo Readme25.txt do diretório Winnt/system32 da seguinte maneira:

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

A URL absoluta na cadeia de conexão especifica o servidor (YourServer) e o caminho (WinNT). Essa URL também define o contexto.

A URL relativa no texto do comando usa a URL absoluta como ponto de partida e especifica o restante do caminho (system32) e o arquivo a ser aberto (Readme25. txt).

O campo opções indica que o tipo de comando é uma URL relativa.

Em outro exemplo, o código a seguir abrirá um **Recordset** no conteúdo do diretório:

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a>Esquemas de URL fornecidos pelo provedor OLE DB

A parte esquerda de uma URL totalmente qualificada, por exemplo, HTTP (HyperText Transfer Protocol) e FTP (File Transfer Protocol), representa o *esquema* usado para acessar o recurso identificado pelo restante da URL.

O ADO oferece suporte aos provedores OLE DB que reconhecem seus próprios esquemas URL. Por exemplo, o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), que acessa arquivos "publicados" do Windows 2000, reconhece o esquema HTTP existente.

