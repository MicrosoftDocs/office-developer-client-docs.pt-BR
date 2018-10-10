---
title: Microsoft OLE DB Provider for Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d5bbc0ab2727a05cb5c140e3aff82778119ad791
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464721"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="9587d-102">Microsoft OLE DB Provider for Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="9587d-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="9587d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9587d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9587d-p101">O Microsoft OLE DB Provider for Internet Publishing permite que o ADO acesse recursos apresentados pelo Microsoft FrontPage ou Microsoft Internet Information Server. Esses recursos incluem arquivos de origem da Web, como arquivos HTML, ou pastas da Web no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9587d-p101">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server. Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="9587d-106">Parâmetros da sequência de conexão</span><span class="sxs-lookup"><span data-stu-id="9587d-106">Connection String Parameters</span></span>

<span data-ttu-id="9587d-107">Para conectar-se a esse provedor, defina o argumento *Provider* da propriedade [ConnectionString](connectionstring-property-ado.md) como:</span><span class="sxs-lookup"><span data-stu-id="9587d-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="9587d-108">Esse valor também pode ser definido ou lido usando a propriedade [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9587d-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="9587d-109">Sequência de conexão típica</span><span class="sxs-lookup"><span data-stu-id="9587d-109">Typical Connection String</span></span>

<span data-ttu-id="9587d-110">Esta é uma sequência de conexão típica para esse provedor:</span><span class="sxs-lookup"><span data-stu-id="9587d-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="9587d-111">\-ou -</span><span class="sxs-lookup"><span data-stu-id="9587d-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="9587d-112">A cadeia de caracteres consiste nas seguintes palavras-chave:</span><span class="sxs-lookup"><span data-stu-id="9587d-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9587d-113">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="9587d-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="9587d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9587d-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9587d-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="9587d-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="9587d-116">Especifica o Microsoft OLE DB Provider for Internet Publishing.</span><span class="sxs-lookup"><span data-stu-id="9587d-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9587d-117"><strong>Data Source</strong> -ou- <strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="9587d-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="9587d-118">Especifica a URL de um arquivo ou o diretório publicado em uma pasta da Web.</span><span class="sxs-lookup"><span data-stu-id="9587d-118">Specifies the URL of a file or directory published in a Web Folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9587d-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="9587d-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="9587d-120">Especifica o nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="9587d-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9587d-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="9587d-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="9587d-122">Especifica a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="9587d-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9587d-p102">Se você especificar um valor inválido ao definir o valor *ResourceURL* no item "URL=" da sequência de conexão, por padrão, o Internet Publishing Provider abrirá uma caixa de diálogo solicitando um valor válido. Esse é um comportamento indesejável para um componente situado na camada intermediária de um aplicativo porque suspende a execução do programa até que a caixa de diálogo seja removida, e o cliente parecerá estar congelado porque não recebeu uma resposta do componente.</span><span class="sxs-lookup"><span data-stu-id="9587d-p102">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value. This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9587d-125">Se MSDAIPP. DSO explicitamente é especificado como o valor do provedor, seja com a palavra-chave de cadeia de caracteres do <EM>provedor de</EM> conexão ou a propriedade <STRONG>Provider</STRONG> , você não pode usar "URL =" na cadeia de conexão.</span><span class="sxs-lookup"><span data-stu-id="9587d-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the <EM>Provider</EM> connection string keyword or the <STRONG>Provider</STRONG> property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="9587d-126">Caso contrário, um erro ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="9587d-126">If you do, an error will occur.</span></span> <span data-ttu-id="9587d-127">Em vez disso, simplesmente especifique a URL, como é mostrado no tópico <A href="the-ole-db-provider-for-internet-publishing.md">Usando o ADO com o OLE DB Provider for Internet Publishing</A>.</span><span class="sxs-lookup"><span data-stu-id="9587d-127">Instead, simply specify the URL as shown in the topic <A href="the-ole-db-provider-for-internet-publishing.md">Using ADO with the OLE DB Provider for Internet Publishing</A>.</span></span></P>


