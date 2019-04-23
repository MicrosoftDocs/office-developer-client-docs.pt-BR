---
title: Microsoft OLE DB Remoting Provider (Provedor de Serviços do ADO)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54ea659aa5392dd4404ffb591eba06f1f9c2910b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288901"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a>Provedor remoto Microsoft OLE DB (Provedor de serviços ADO)

**Aplica-se ao:** Access 2013, Office 2013

O Microsoft OLE DB Remoting Provider permite que um usuário local em uma máquina cliente invoque provedores de dados em uma máquina remota. Especifique os parâmetros do provedor de dados na máquina remota como se fosse um usuário local na máquina remota. Em seguida, especifique os parâmetros utilizados pelo Remoting Provider para acessar a máquina remota. Como resultado, você acessará a máquina remota como se fosse um usuário local.

## <a name="provider-keyword"></a>Palavra-chave do provedor

Para invocar o OLE DB Remoting Provider, especifique a palavra-chave e o valor abaixo na sequência de conexão. (Observe o espaço em branco no nome do provedor.)

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a>Palavras-chave adicionais

Quando esse provedor de serviços é invocado, as seguintes palavras-chave adicionais são relevantes:

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
<td><p><strong>Data Source</strong></p></td>
<td><p>Especifica o nome da fonte de dados remota. É passada ao OLE DB Remoting Provider para processamento. Essa palavra-chave é equivalente à propriedade <a href="connect-property-rds.md">Connect</a> do objeto <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a>Propriedades dinâmicas

Quando esse provedor de serviços é invocado, as propriedades dinâmicas abaixo são adicionadas à coleção [Properties](connection-object-ado.md) do objeto [Connection](properties-collection-ado.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da propriedade dinâmica</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>DFMode</strong></p></td>
<td><p>Indica o Modo DataFactory. Uma cadeia de caracteres que especifica a versão desejada do objeto <a href="datafactory-object-rdsserver.md">DataFactory</a> no servidor. Defina esta propriedade antes de abrir uma conexão para solicitar uma versão específica de <strong>DataFactory</strong>. Se a versão solicitada não estiver disponível, será feita uma tentativa de usar a versão anterior. Se não houver uma versão anterior, ocorrerá um erro. Se <strong>DFMode</strong> for inferior à versão disponível, ocorrerá um erro. Esta propriedade será somente leitura depois que uma conexão for estabelecida. Pode ser um dos seguintes valores válidos da cadeia de caracteres:</p>
<p></p>
<ul>
<li><p>&quot;25&quot; – versão 2,5 (padrão)</p></li>
<li><p>&quot;21&quot; — versão 2,1</p></li>
<li><p>&quot;20&quot; — versão 2,0</p></li>
<li><p>&quot;15&quot; – versão 1,5</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Command Properties</strong></p></td>
<td><p>Indica os valores que serão adicionados à sequência de propriedades de comando (conjunto de linhas) enviadas ao servidor pelo provedor MS Remote. O valor padrão para essa cadeia de caracteres é vt_empty.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Current DFMode</strong></p></td>
<td><p>Indica o número da versão do <strong>DataFactory</strong> existente no servidor. Verifique esta propriedade para determinar se a versão solicitada na propriedade <strong>DFMode</strong> foi considerada. Pode ser um dos seguintes valores inteiros longos válidos:</p>
<p></p>
<ul>
<li><p>25 — Versão 2.5 (Padrão)</p></li>
<li><p>21 — Versão 2.1</p></li>
<li><p>20 — Versão 2.0</p></li>
<li><p>15 — Versão 1.5</p></li>
</ul>
<p></p>
<p>Adição &quot;de DFMode = 20; &quot; para a cadeia de conexão ao usar o provedor <strong>MSRemote</strong> pode melhorar o desempenho do seu servidor ao atualizar dados. Com essa definição, o objeto <strong>RDSServer.DataFactory</strong> do servidor usa um modo de recursos menos intensivo. No entanto, os seguintes recursos não estão disponíveis nesta configuração:</p>
<p></p>
<ul>
<li><p>Uso de consultas parametrizadas.</p></li>
<li><p>Obtenção de informações de parâmetro ou de coluna antes da chamada do método <strong>Execute</strong>.</p></li>
<li><p>Definição de <strong>Transacionar Atualizações</strong> como <strong>Verdadeira</strong>.</p></li>
<li><p>Obtenção de status da linha.</p></li>
<li><p>Chamada do método <strong>Resync</strong>.</p></li>
<li><p>Atualização (de forma explícita ou automática) por meio da propriedade <strong>Update Resync</strong>.</p></li>
<li><p>Definição das propriedades <strong>Command</strong> ou <strong>Recordset</strong>.</p></li>
<li><p>Usar <strong>adCmdTableDirect</strong>.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Indicador</strong></p></td>
<td><p>Indica o nome de um programa de personalização do servidor (ou manipulador) que estende a funcionalidade do <a href="datafactory-object-rdsserver.md">RDSServer.</a>datafactory e quaisquer parâmetros usados pelo manipulador<em>,</em> todos separados por vírgulas (&quot;,&quot;). Um valor <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Internet Timeout</strong></p></td>
<td><p>Indica o intervalo máximo de espera, em milissegundos, pelo ciclo completo de envio da solicitação e resposta do servidor. (O padrão é 5 minutos.)</p></td>
</tr>
<tr class="even">
<td><p><strong>Remote Provider</strong></p></td>
<td><p>Indica o nome do provedor de dados que será utilizado no servidor remoto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Remote Server</strong></p></td>
<td><p>Indica o nome do servidor e o protocolo de comunicação que será utilizado nessa conexão. Esta propriedade é equivalente à propriedade <a href="server-property-rds.md">Server</a> do objeto <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Transact Updates</strong></p></td>
<td><p>Se tiver sido definido como True, este valor indicará que quando <a href="updatebatch-method-ado.md">UpdateBatch</a> for executado no servidor, isso ocorrerá dentro de uma transação. O valor padrão para essa propriedade dinâmica booleana é False.</p></td>
</tr>
</tbody>
</table>


Você também pode definir propriedades dinâmicas que podem ser gravadas especificando seus nomes como palavras-chave na sequência de conexão. Por exemplo, defina o valor de cinco segundos para a propriedade dinâmica **Internet Timeout**, especificando:

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

Além disso, você pode definir ou recuperar uma propriedade dinâmica especificando o seu nome como índice da propriedade **Properties**. Por exemplo, obtenha e imprima o valor atual da propriedade dinâmica **Internet Timeout** e defina um novo valor, como este:

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a>Comentários

No ADO 2.0, o OLE DB Remoting Provider podia ser especificado somente no parâmetro *ActiveConnection* do método **Open** do objeto [Recordset](recordset-object-ado.md). A partir do ADO 2.1, o provedor também pode ser especificado no parâmetro *ConnectionString* do método **Open** do objeto [Connection](connection-object-ado.md).

O equivalente da propriedade [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) do objeto **RDS.DataControl** não está disponível. Em seu lugar é utilizado o argumento *Source* do método **Open** do objeto [Recordset](recordset-object-ado.md).

Especificar "...;Remote Provider=MS Remote;..." criaria um cenário em quatro camadas. Os cenários com mais de três camadas não foram testados e não devem ser necessários.

## <a name="example"></a>Exemplo

Este exemplo executa uma consulta na tabela **authors** do banco de dados **pubs** em um servidor chamado *YourServer*. Os nomes da fonte de dados remota e do servidor remoto são fornecidos no método [Open](open-method-ado-connection.md) do objeto [Connection](connection-object-ado.md) e a consulta SQL é especificada no método [Open](open-method-ado-recordset.md) do objeto [Recordset](recordset-object-ado.md). Um objeto **Recordset** é retornado, editado e usado para atualizar a fonte de dados.

```vb 
 
Dim rs as New ADODB.Recordset 
Dim cn as New ADODB.Connection 
cn.Open  "Provider=MS Remote;Data Source=pubs;" & _ 
         "Remote Server=https://YourServer" 
rs.Open "SELECT * FROM authors", cn 
...                'Edit the recordset 
rs.UpdateBatch     'Equivalent of RDS SubmitChanges 
... 
```

