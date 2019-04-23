---
title: Microsoft OLE DB Provider for Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 38183cd8306f2425a362bd2650639120a2d16845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288964"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a>Microsoft OLE DB Provider para Publicação de Internet

**Aplica-se ao:** Access 2013, Office 2013

O Microsoft OLE DB Provider for Internet Publishing permite que o ADO acesse recursos apresentados pelo Microsoft FrontPage ou Microsoft Internet Information Server. Esses recursos incluem arquivos de origem da Web, como arquivos HTML, ou pastas da Web no Windows 2000.

## <a name="connection-string-parameters"></a>Parâmetros de cadeia de conexão

Para estabelecer uma conexão com esse provedor, defina o argumento *Provider* da propriedade [ConnectionString](connectionstring-property-ado.md) como:

```vb 
 
MSDAIPP.DSO 
```

Esse valor também pode ser definido ou lido usando a propriedade [Provider](provider-property-ado.md).

## <a name="typical-connection-string"></a>Cadeia de conexão típica

Esta é uma sequência de conexão típica para esse provedor:

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

\-ou

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
<td><p>Especifica a URL de um arquivo ou diretório publicado em uma pasta da Web.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ID de usuário</strong></p></td>
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
> Se MSDAIPP.DSO for especificado explicitamente como o valor do provedor, seja através da palavra-chave *Provider* na sequência de conexão ou através da propriedade **Provider**, você não poderá usar "URL=" na sequência de conexão. Caso contrário, um erro ocorrerá. Em vez disso, simplesmente especifique a URL, como é mostrado no tópico [Usando o ADO com o OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).

