---
title: Microsoft OLE DB Provider for Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6f1c7c65d0ac1dd2a6d3ea132a31955f175bc7f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997480"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a>Microsoft OLE DB Provider for Internet Publishing

**Aplica-se a**: Access 2013, o Office 2013

O Microsoft OLE DB Provider for Internet Publishing permite que o ADO acesse recursos apresentados pelo Microsoft FrontPage ou Microsoft Internet Information Server. Esses recursos incluem arquivos de origem da Web, como arquivos HTML, ou pastas da Web no Windows 2000.

## <a name="connection-string-parameters"></a>Parâmetros da cadeia de Conexão

Para conectar-se a esse provedor, defina o argumento *Provider* da propriedade [ConnectionString](connectionstring-property-ado.md) como:

```vb 
 
MSDAIPP.DSO 
```

Esse valor também pode ser definido ou lido usando a propriedade [Provider](provider-property-ado.md).

## <a name="typical-connection-string"></a>Cadeia de caracteres de conexão típica

Esta é uma sequência de conexão típica para esse provedor:

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

\-ou -

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

A cadeia de caracteres consiste nas seguintes palavras-chave:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Palavra-chave</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Especifica o Microsoft OLE DB Provider for Internet Publishing.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong> -ou- <strong>URL</strong></p></td>
<td><p>Especifica a URL de um arquivo ou diretório publicado em uma pasta da web.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User ID</strong></p></td>
<td><p>Especifica o nome do usuário.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Especifica a senha do usuário.</p></td>
</tr>
</tbody>
</table>


Se você especificar um valor inválido ao definir o valor *ResourceURL* no item "URL=" da sequência de conexão, por padrão, o Internet Publishing Provider abrirá uma caixa de diálogo solicitando um valor válido. Esse é um comportamento indesejável para um componente situado na camada intermediária de um aplicativo porque suspende a execução do programa até que a caixa de diálogo seja removida, e o cliente parecerá estar congelado porque não recebeu uma resposta do componente.

> [!NOTE]
> Se MSDAIPP. DSO explicitamente é especificado como o valor do provedor, seja com a palavra-chave de cadeia de caracteres do *provedor de* conexão ou a propriedade **Provider** , você não pode usar "URL =" na cadeia de conexão. Caso contrário, um erro ocorrerá. Em vez disso, simplesmente especifique a URL, como é mostrado no tópico [Usando o ADO com o OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).

