---
title: Propriedade ConnectionString (ADO)
TOCTitle: ConnectionString Property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90e884f821c3ca7667020ffe041b4e064555c02b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464556"
---
# <a name="connectionstring-property-ado"></a>Propriedade ConnectionString (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica as informações usadas para estabelecer uma conexão com uma fonte de dados.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String**.

## <a name="remarks"></a>Comentários

Use a propriedade **ConnectionString** para especificar uma fonte de dados passando uma cadeia de caracteres de conexão detalhada contendo uma série de instruções de *= o valor* do *argumento* separados por ponto e vírgula.

O ADO oferece suporte a cinco argumentos para a propriedade **ConnectionString**; quaisquer outros argumentos são passados diretamente para o provedorsem serem processados pelo ADO. Os argumentos aos quais o ADO oferece suporte são os seguintes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Provider=</em></p></td>
<td><p>Especifica o nome de um provedor a ser usado para a conexão.</p></td>
</tr>
<tr class="even">
<td><p><em>Nome do arquivo =</em></p></td>
<td><p>Especifica o nome de um arquivo específico do provedor (por exemplo, um objeto de fonte de dados persistente) contendo informações de conexão predefinidas.</p></td>
</tr>
<tr class="odd">
<td><p><em>Remote Provider =</em></p></td>
<td><p>Especifica o nome do provedor a ser usado ao abrir uma conexão no cliente (somente Remote Data Service).</p></td>
</tr>
<tr class="even">
<td><p><em>Servidor remoto =</em></p></td>
<td><p>Especifica o nome do caminho do servidor a ser usado ao abrir uma conexão do lado do cliente. (Apenas para o Remote Data Service.)</p></td>
</tr>
<tr class="odd">
<td><p><em>URL=</em></p></td>
<td><p>Especifica a cadeia de caracteres de conexão como uma URL absoluta que identifica um recurso, como um arquivo ou diretório.</p></td>
</tr>
</tbody>
</table>


Depois que a propriedade **ConnectionString** for definida e o objeto [Connection](connection-object-ado.md) aberto, o provedor poderá alterar o conteúdo da propriedade, por exemplo, mapeando os nomes de argumento definidos pelo ADO para os seus equivalentes no provedor.

A propriedade **ConnectionString** herda automaticamente o valor usado para o argumento *ConnectionString* do método [Open](open-method-ado-connection.md) , portanto, você pode substituir a propriedade **ConnectionString** atual durante a chamada do método **Open** .

Como o argumento *File Name* faz com que o ADO carregue o provedor associado, você não pode passar o *provedor* e o *Nome do arquivo* de argumentos.

A propriedade **ConnectionString** será leitura/gravação quando a conexão estiver fechada e somente leitura quando estiver aberta.

As duplicatas de um argumento na propriedade **ConnectionString** serão ignoradas. A última instância do argumento será usada.

**Uso de serviço de dados remotos** Quando usado em um objeto de **Conexão** do cliente, a propriedade **ConnectionString** pode incluir apenas os parâmetros *Remote Provider* e *Remote Server* .

