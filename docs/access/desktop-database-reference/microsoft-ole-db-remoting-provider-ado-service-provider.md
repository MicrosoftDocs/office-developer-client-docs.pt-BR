---
title: Microsoft OLE DB Remoting Provider (Provedor de Serviços do ADO)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 07031639b707fc24a3e5b057520c601c9472b01b
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026313"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a><span data-ttu-id="c73a2-102">Microsoft OLE DB Remoting Provider (Provedor de Serviços do ADO)</span><span class="sxs-lookup"><span data-stu-id="c73a2-102">Microsoft OLE DB Remoting Provider (ADO Service Provider)</span></span>

<span data-ttu-id="c73a2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c73a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c73a2-p101">O Microsoft OLE DB Remoting Provider permite que um usuário local em uma máquina cliente invoque provedores de dados em uma máquina remota. Especifique os parâmetros do provedor de dados na máquina remota como se fosse um usuário local na máquina remota. Em seguida, especifique os parâmetros utilizados pelo Remoting Provider para acessar a máquina remota. Como resultado, você acessará a máquina remota como se fosse um usuário local.</span><span class="sxs-lookup"><span data-stu-id="c73a2-p101">The Microsoft OLE DB Remoting Provider enables a local user on a client machine to invoke data providers on a remote machine. Specify the data provider parameters for the remote machine as you would if you were a local user on the remote machine. Then specify the parameters used by the Remoting Provider to access the remote machine. The resulting effect is that you will access the remote machine as if you were a local user.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="c73a2-108">Palavra-chave do provedor</span><span class="sxs-lookup"><span data-stu-id="c73a2-108">Provider Keyword</span></span>

<span data-ttu-id="c73a2-p102">Para invocar o OLE DB Remoting Provider, especifique a palavra-chave e o valor abaixo na sequência de conexão. (Observe o espaço em branco no nome do provedor.)</span><span class="sxs-lookup"><span data-stu-id="c73a2-p102">To invoke the OLE DB Remoting Provider, specify the following keyword and value in the connection string. (Note the blank space in the provider name.)</span></span>

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a><span data-ttu-id="c73a2-111">Palavras-chave adicionais</span><span class="sxs-lookup"><span data-stu-id="c73a2-111">Additional Keywords</span></span>

<span data-ttu-id="c73a2-112">Quando esse provedor de serviços é invocado, as seguintes palavras-chave adicionais são relevantes:</span><span class="sxs-lookup"><span data-stu-id="c73a2-112">When this service provider is invoked, the following additional keywords are relevant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c73a2-113">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="c73a2-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="c73a2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c73a2-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c73a2-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="c73a2-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="c73a2-116">Especifica o nome da fonte de dados remota.</span><span class="sxs-lookup"><span data-stu-id="c73a2-116">Specifies the name of the remote data source.</span></span> <span data-ttu-id="c73a2-117">Ele é passado para o provedor OLE DB Remoting para processamento.</span><span class="sxs-lookup"><span data-stu-id="c73a2-117">It is passed to the OLE DB Remoting Provider for processing.</span></span> <span data-ttu-id="c73a2-118">Essa palavra-chave é equivalente à propriedade <a href="connect-property-rds.md">Connect</a> do objeto <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</span><span class="sxs-lookup"><span data-stu-id="c73a2-118">This keyword is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object's <a href="connect-property-rds.md">Connect</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a><span data-ttu-id="c73a2-119">Propriedades dinâmicas</span><span class="sxs-lookup"><span data-stu-id="c73a2-119">Dynamic Properties</span></span>

<span data-ttu-id="c73a2-120">Quando esse provedor de serviços é invocado, as propriedades dinâmicas abaixo são adicionadas à coleção [Properties](connection-object-ado.md) do objeto [Connection](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c73a2-120">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c73a2-121">Nome da propriedade dinâmica</span><span class="sxs-lookup"><span data-stu-id="c73a2-121">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="c73a2-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="c73a2-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c73a2-123"><strong>DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="c73a2-123"><strong>DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="c73a2-124">Indica o modo de DataFactory.</span><span class="sxs-lookup"><span data-stu-id="c73a2-124">Indicates the DataFactory Mode.</span></span> <span data-ttu-id="c73a2-125">Uma string que especifica a versão desejada do objeto <a href="datafactory-object-rdsserver.md">DataFactory</a> no servidor.</span><span class="sxs-lookup"><span data-stu-id="c73a2-125">A string that specifies the desired version of the <a href="datafactory-object-rdsserver.md">DataFactory</a> object on the server.</span></span> <span data-ttu-id="c73a2-126">Defina essa propriedade antes de abrir uma conexão para solicitar uma versão específica do <strong>DataFactory</strong>.</span><span class="sxs-lookup"><span data-stu-id="c73a2-126">Set this property before opening a connection to request a particular version of the <strong>DataFactory</strong>.</span></span> <span data-ttu-id="c73a2-127">Se a versão solicitada não estiver disponível, será feita uma tentativa de usar a versão anterior.</span><span class="sxs-lookup"><span data-stu-id="c73a2-127">If the requested version is not available, an attempt will be made to use the preceding version.</span></span> <span data-ttu-id="c73a2-128">Se não houver nenhuma versão anterior, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="c73a2-128">If there is no preceding version, an error will occur.</span></span> <span data-ttu-id="c73a2-129">Se <strong>DFMode</strong> for menor que a versão disponível, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="c73a2-129">If <strong>DFMode</strong> is less than the available version, an error will occur.</span></span> <span data-ttu-id="c73a2-130">Essa propriedade é somente leitura depois que uma conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="c73a2-130">This property is read-only after a connection is made.</span></span> <span data-ttu-id="c73a2-131">Pode ser um dos seguintes valores válidos da cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="c73a2-131">Can be one of the following valid string values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="c73a2-132">&quot;25&quot; — versão 2.5 (padrão)</span><span class="sxs-lookup"><span data-stu-id="c73a2-132">&quot;25&quot; — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="c73a2-133">&quot;21&quot; — versão 2.1</span><span class="sxs-lookup"><span data-stu-id="c73a2-133">&quot;21&quot; — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="c73a2-134">&quot;20&quot; — versão 2.0</span><span class="sxs-lookup"><span data-stu-id="c73a2-134">&quot;20&quot; — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="c73a2-135">&quot;15&quot; — versão 1.5</span><span class="sxs-lookup"><span data-stu-id="c73a2-135">&quot;15&quot; — Version 1.5</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73a2-136"><strong>Command Properties</strong></span><span class="sxs-lookup"><span data-stu-id="c73a2-136"><strong>Command Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="c73a2-p105">Indica os valores que serão adicionados à sequência de propriedades de comando (conjunto de linhas) enviadas ao servidor pelo provedor MS Remote. O valor padrão para essa cadeia de caracteres é vt_empty.</span><span class="sxs-lookup"><span data-stu-id="c73a2-p105">Indicates values that will be added to the string of command (rowset) properties sent to the server by the MS Remote provider. The default value for this string is vt_empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73a2-139"><strong>Current DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="c73a2-139"><strong>Current DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="c73a2-140">Indica o número de versão real do <strong>DataFactory</strong> no servidor.</span><span class="sxs-lookup"><span data-stu-id="c73a2-140">Indicates the actual version number of the <strong>DataFactory</strong> on the server.</span></span> <span data-ttu-id="c73a2-141">Verificar essa propriedade para ver se a versão solicitada na propriedade <strong>DFMode</strong> foi cumprida.</span><span class="sxs-lookup"><span data-stu-id="c73a2-141">Check this property to see if the version requested in the <strong>DFMode</strong> property was honored.</span></span> <span data-ttu-id="c73a2-142">Pode ser um dos seguintes valores inteiros longos válidos:</span><span class="sxs-lookup"><span data-stu-id="c73a2-142">Can be one of the following valid Long integer values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="c73a2-143">25 — Versão 2.5 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c73a2-143">25 — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="c73a2-144">21 — Versão 2.1</span><span class="sxs-lookup"><span data-stu-id="c73a2-144">21 — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="c73a2-145">20 — Versão 2.0</span><span class="sxs-lookup"><span data-stu-id="c73a2-145">20 — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="c73a2-146">15 — Versão 1.5</span><span class="sxs-lookup"><span data-stu-id="c73a2-146">15 — Version 1.5</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="c73a2-147">Adicionando &quot;DFMode = 20; &quot; para sua conexão cadeia de caracteres ao usar o provedor <strong>MSRemote</strong> pode melhorar o desempenho do seu servidor durante uma atualização de dados.</span><span class="sxs-lookup"><span data-stu-id="c73a2-147">Adding &quot;DFMode=20;&quot; to your connection string when using the <strong>MSRemote</strong> provider can improve your server's performance when updating data.</span></span> <span data-ttu-id="c73a2-148">Com essa definição, o objeto <strong>RDSServer.DataFactory</strong> do servidor usa um modo de recursos menos intensivo.</span><span class="sxs-lookup"><span data-stu-id="c73a2-148">With this setting, the <strong>RDSServer.DataFactory</strong> object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="c73a2-149">No entanto, os seguintes recursos não estão disponíveis nesta configuração:</span><span class="sxs-lookup"><span data-stu-id="c73a2-149">However, the following features are not available in this configuration:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="c73a2-150">Uso de consultas parametrizadas.</span><span class="sxs-lookup"><span data-stu-id="c73a2-150">Using parameterized queries.</span></span></p></li>
<li><p><span data-ttu-id="c73a2-151">Obtenção de informações de parâmetro ou de coluna antes da chamada do método <strong>Execute</strong>.</span><span class="sxs-lookup"><span data-stu-id="c73a2-151">Getting parameter or column information before calling the <strong>Execute</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="c73a2-152">Definição de <strong>Transacionar Atualizações</strong> como <strong>Verdadeira</strong>.</span><span class="sxs-lookup"><span data-stu-id="c73a2-152">Setting <strong>Transact Updates</strong> to <strong>True</strong>.</span></span></p></li>
<li><p><span data-ttu-id="c73a2-153">Obtenção de status da linha.</span><span class="sxs-lookup"><span data-stu-id="c73a2-153">Getting row status.</span></span></p></li>
<li><p><span data-ttu-id="c73a2-154">Chamada do método <strong>Resync</strong>.</span><span class="sxs-lookup"><span data-stu-id="c73a2-154">Calling the <strong>Resync</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="c73a2-155">Atualização (de forma explícita ou automática) por meio da propriedade <strong>Update Resync</strong>.</span><span class="sxs-lookup"><span data-stu-id="c73a2-155">Refreshing (explicitly or automatically) via the <strong>Update Resync</strong> property.</span></span></p></li>
<li><p><span data-ttu-id="c73a2-156">Definição das propriedades <strong>Command</strong> ou <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c73a2-156">Setting <strong>Command</strong> or <strong>Recordset</strong> properties.</span></span></p></li>
<li><p><span data-ttu-id="c73a2-157">Uso de <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="c73a2-157">Using <strong>adCmdTableDirect</strong>.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73a2-158"><strong>Manipulador</strong></span><span class="sxs-lookup"><span data-stu-id="c73a2-158"><strong>Handler</strong></span></span></p></td>
<td><p><span data-ttu-id="c73a2-159">Indica o nome de um programa de personalização do lado do servidor (ou manipulador) que estende a funcionalidade do <a href="datafactory-object-rdsserver.md">rdsserver. DataFactory</a>e qualquer parâmetro usado pelo manipulador<em>,</em> todos separado por vírgulas (&quot;,&quot;).</span><span class="sxs-lookup"><span data-stu-id="c73a2-159">Indicates the name of a server-side customization program (or handler) that extends the functionality of the <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>, and any parameters used by the handler<em>,</em> all separated by commas (&quot;,&quot;).</span></span> <span data-ttu-id="c73a2-160">Um valor <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="c73a2-160">A <strong>String</strong> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73a2-161"><strong>Internet Timeout</strong></span><span class="sxs-lookup"><span data-stu-id="c73a2-161"><strong>Internet Timeout</strong></span></span></p></td>
<td><p><span data-ttu-id="c73a2-p109">Indica o intervalo máximo de espera, em milissegundos, pelo ciclo completo de envio da solicitação e resposta do servidor. (O padrão é 5 minutos.)</span><span class="sxs-lookup"><span data-stu-id="c73a2-p109">Indicates the maximum number of milliseconds to wait for a request to travel to and from the server. (The default is 5 minutes.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73a2-164"><strong>Remote Provider</strong></span><span class="sxs-lookup"><span data-stu-id="c73a2-164"><strong>Remote Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="c73a2-165">Indica o nome do provedor de dados que será utilizado no servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="c73a2-165">Indicates the name of the data provider to be used on the remote server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c73a2-166"><strong>Remote Server</strong></span><span class="sxs-lookup"><span data-stu-id="c73a2-166"><strong>Remote Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c73a2-p110">Indica o nome do servidor e o protocolo de comunicação que será utilizado nessa conexão. Esta propriedade é equivalente à propriedade <a href="server-property-rds.md">Server</a> do objeto <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</span><span class="sxs-lookup"><span data-stu-id="c73a2-p110">Indicates the server name and communication protocol to be used by this connection. This property is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object <a href="server-property-rds.md">Server</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c73a2-169"><strong>Transact Updates</strong></span><span class="sxs-lookup"><span data-stu-id="c73a2-169"><strong>Transact Updates</strong></span></span></p></td>
<td><p><span data-ttu-id="c73a2-p111">Se tiver sido definido como True, este valor indicará que quando <a href="updatebatch-method-ado.md">UpdateBatch</a> for executado no servidor, isso ocorrerá dentro de uma transação. O valor padrão para essa propriedade dinâmica booleana é False.</span><span class="sxs-lookup"><span data-stu-id="c73a2-p111">When set to True, this value indicates that when <a href="updatebatch-method-ado.md">UpdateBatch</a> is performed on the server, it will be done inside a transaction. The default value for this Boolean dynamic property is False.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c73a2-p112">Você também pode definir propriedades dinâmicas que podem ser gravadas especificando seus nomes como palavras-chave na sequência de conexão. Por exemplo, defina o valor de cinco segundos para a propriedade dinâmica **Internet Timeout**, especificando:</span><span class="sxs-lookup"><span data-stu-id="c73a2-p112">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, set the **Internet Timeout** dynamic property to five seconds by specifying:</span></span>

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

<span data-ttu-id="c73a2-p113">Além disso, você pode definir ou recuperar uma propriedade dinâmica especificando o seu nome como índice da propriedade **Properties**. Por exemplo, obtenha e imprima o valor atual da propriedade dinâmica **Internet Timeout** e defina um novo valor, como este:</span><span class="sxs-lookup"><span data-stu-id="c73a2-p113">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** property. For example, get and print the current value of the **Internet Timeout** dynamic property, and then set a new value, like this:</span></span>

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a><span data-ttu-id="c73a2-176">Comentários</span><span class="sxs-lookup"><span data-stu-id="c73a2-176">Remarks</span></span>

<span data-ttu-id="c73a2-177">No ADO 2.0, o OLE DB Remoting Provider só pode ser especificado no parâmetro *ActiveConnection* do método **Open** do objeto [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c73a2-177">In ADO 2.0, the OLE DB Remoting Provider could only be specified in the *ActiveConnection* parameter of the [Recordset](recordset-object-ado.md) object **Open** method.</span></span> <span data-ttu-id="c73a2-178">Iniciando com o ADO 2.1, o provedor também pode ser especificado no parâmetro *ConnectionString* do método **Open** do objeto de [Conexão](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c73a2-178">Starting with ADO 2.1, the provider may also be specified in the *ConnectionString* parameter of the [Connection](connection-object-ado.md) object **Open** method.</span></span>

<span data-ttu-id="c73a2-179">O equivalente da propriedade **SQL** do objeto [RDS.DataControl](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) não está disponível.</span><span class="sxs-lookup"><span data-stu-id="c73a2-179">The equivalent of the **RDS.DataControl** object [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property is not available.</span></span> <span data-ttu-id="c73a2-180">O argumento *Source* do método **Open** do objeto [Recordset](recordset-object-ado.md) é usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c73a2-180">The [Recordset](recordset-object-ado.md) object **Open** method *Source* argument is used instead.</span></span>

<span data-ttu-id="c73a2-181">Especificar "...;Remote Provider=MS Remote;..." criaria um cenário em quatro camadas. Os cenários com mais de três camadas não foram testados e não devem ser necessários.</span><span class="sxs-lookup"><span data-stu-id="c73a2-181">Specifying "...;Remote Provider=MS Remote;..." would create a four-tier scenario.Scenarios beyond three tiers have not been tested and should not be needed.</span></span>

## <a name="example"></a><span data-ttu-id="c73a2-182">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c73a2-182">Example</span></span>

<span data-ttu-id="c73a2-p116">Este exemplo executa uma consulta na tabela **authors** do banco de dados **pubs** em um servidor chamado *YourServer*. Os nomes da fonte de dados remota e do servidor remoto são fornecidos no método [Open](open-method-ado-connection.md) do objeto [Connection](connection-object-ado.md) e a consulta SQL é especificada no método [Open](open-method-ado-recordset.md) do objeto [Recordset](recordset-object-ado.md). Um objeto **Recordset** é retornado, editado e usado para atualizar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="c73a2-p116">This example performs a query on the **authors** table of the **pubs** database on a server named, *YourServer*. The names of the remote data source and remote server are provided in the [Connection](connection-object-ado.md) object [Open](open-method-ado-connection.md) method, and the SQL query is specified in the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method. A **Recordset** object is returned, edited, and used to update the data source.</span></span>

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

