---
title: 'Capítulo 12: tutorial do RDS (Remote Data Service)'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296476"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a>Capítulo 12: tutorial do RDS (Remote Data Service)

**Aplica-se ao:** Access 2013, Office 2013

Este tutorial ilustra o uso do modelo de programação RDS para consultar e atualizar uma fonte de dados. Primeiramente, ele descreve as etapas necessárias para realizar essa tarefa. Em seguida, o tutorial é repetido no Microsoft Visual Basic Scripting Edition e no Microsoft Visual J++, apresentando o ADO for Windows Foundation classes (ADO/WFC).

Este tutorial é codificado em diferentes linguagens por dois motivos:

- A documentação do RDS assume os códigos do leitor no Visual Basic. Isso torna a documentação conveniente para programadores do Visual Basic, mas menos útil para os programadores que utilizam outras linguagens.

- Se você não estiver certo quanto a um determinado recurso RDS e conhecer um pouco de outra linguagem, pode conseguir resolver sua questão para o mesmo recurso expresso em outra linguagem.

Esse tutorial é baseado no modelo de programação RDS. Ele discute cada etapa do modelo de programação individualmente. Além disso, ilustra cada etapa com um fragmento do código do Visual Basic.

O exemplo do código é repetido em outras linguagens com a discussão mínima. Cada etapa em um determinado tutorial de linguagem de programação está marcado com a etapa correspondente no modelo de programação e tutorial descritivo. Utilize o número da etapa para se referir à discussão no tutorial descritivo.

O modelo de programação RDS está indicado abaixo. Utilize-o como um roteiro conforme avança no tutorial.

### <a name="rds-programming-model-with-objects"></a>Modelo de programação do RDS com objetos

- Especifique o programa a ser chamado no servidor e obtenha uma maneira (proxy) de se referir a ele a partir do cliente.

- Chame o programa do servidor. Transmita os parâmetros ao programa do servidor que identifica a fonte de dados e o comando a ser emitido.

- O programa do servidor obtém um objeto [Recordset](recordset-object-ado.md) da fonte de dados, geralmente usando o ADO. Opcionalmente, o objeto **Recordset** é processado no servidor.

- O programa do servidor retorna o objeto **Recordset** final ao aplicativo cliente.

- No cliente, o objeto **Recordset** é colocado opcionalmente em um formulário que pode ser facilmente usado por controle visuais.

- As alterações ao objeto **Recordset** são enviadas de volta ao servidor e utilizadas para atualizar a fonte de dados.

## <a name="step-1-specify-a-server-program"></a>Etapa 1: especificar um programa de servidor

No caso mais geral, use o objeto [RDS.DataSpace](dataspace-object-rds.md) do método [CreateObject](createobject-method-rds.md) para especificar o programa do servidor padrão, [RDSServer.DataFactory](datafactory-object-rdsserver.md), ou seu próprio programa de servidor personalizado (objeto de negócios). Um programa de servidor é instanciado no servidor e uma referência ao programa do servidor, ou *proxy*, é retornada.

Este tutorial usa o programa do servidor padrão:

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a>Etapa 2: chamar o programa do servidor 

Ao chamar um método no *proxy* do cliente, o programa real no servidor executa o método. Nessa etapa, você executará uma consulta no servidor.

### <a name="part-a"></a>Parte A 

Se você não não usou o [RDSServer.DataFactory](datafactory-object-rdsserver.md) nesse tutorial, a maneira mais conveniente de executar essa etapa seria usar o objeto [RDS.DataControl](datacontrol-object-rds.md). O **RDS.DataControl** combina a etapa anterior da criação de um proxy, com essa etapa, emitindo a consulta.

1. Defina o **RDS. **Propriedade do [servidor](server-property-rds.md) de objeto DataControl para identificar onde o programa do servidor deve ser instanciado.

2. Defina a propriedade [Connect](connect-property-rds.md) para especificar a cadeia de conexão para acessar a fonte de dados.

3. Defina a propriedade [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) para especificar o texto do comando de consulta. 

4. Execute o método [Refresh](refresh-method-rds.md) para fazer com que o programa de servidor se conecte à fonte de dados, recupere as linhas especificadas pela consulta e retorne um objeto **Recordset** para o cliente.

Este tutorial não usa o **RDS.DataControl**, mas veja como seria se o fizesse:

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

Ele também não invoca RDS com objetos ADO, mas veja como seria se o fizesse:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a>Parte B 

O método geral para executar esta etapa é invocar o método [Query](query-method-rds.md) do objeto**RDSServer.DataFactory**. Esse método assume uma cadeia de conexão, que é usada para se conectar a uma origem de dados e um texto de comando, que é usada para especificar as linhas a serem retornadas a partir da origem de dados.

Este tutorial usa o método **Query** do objeto **DataFactory**:

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a>Etapa 3: o servidor Obtém um Recordset 

O programa do servidor usa a sequência de conexão e o texto de comando para consultar a fonte de dados para as linhas desejadas. O ADO geralmente é usado para recuperar esse **Recordset**, embora outras interfaces de acesso a dados da Microsoft, como o OLE DB, podem ser usadas.

Um programa de servidor personalizado pode parecer com:

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a>Etapa 4: o servidor retorna o Recordset 

O RDS converte o objeto **Recordset** recuperado para um formato que pode ser enviado de volta ao cliente (ou seja, ele *empacota* o **Recordset**). O formato exato da conversão e como ele é gasto depende de o servidor estar na Internet ou na intranet, uma rede local ou é uma biblioteca de vínculos dinâmicos. Contudo, este detalhe não é crítico; o que importa é que o RDS envia o **Recordset** de volta ao cliente.

No lado cliente, um objeto **Recordset** é retornado e atribuído a uma variável local.

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a>Etapa 5: o dataControl é tornado utilizável 

O objeto **Recordset** retornado está disponível para uso. Você pode examinar, navegar ou editá-lo como faria com qualquer outro **Recordset**. As possibilidades de uso do **Recordset** dependem do seu ambiente. O Visual Basic e o Visual C++ possuem controles visuais que podem utilizar um **Recordset** diretamente ou indiretamente com a ajuda de um controle de dados de ativação.

Por exemplo, se você estiver exibindo uma página da Web no Internet Explorer, talvez queira exibir os dados do objeto **Recordset** em um controle visual. Os controles visuais em uma página da Web não podem acessar um objeto **Recordset** diretamente. No entanto, podem acessar o objeto **Recordset** através do [RDS.DataControl](datacontrol-object-rds.md). O **RDS.DataControl** torna-se utilizável por um controle visual quando sua propriedade [SourceRecordset](recordset-sourcerecordset-properties-rds.md) for definida como o objeto **Recordset**.

O objeto de controle visual deve ter seu parâmetro **DATASRC** definido como **RDS.DataControl** e sua propriedade **DATAFLD** definida como um campo de objeto **Recordset** (coluna).

Nesse tutorial, defina a propriedade **SourceRecordset**:

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a>Etapa 6: as alterações são enviadas ao servidor

Se o objeto **Recordset** for editado, todas as alterações (ou seja, linhas que são incluídas, alteradas ou excluídas) poderão ser enviadas de volta ao servidor.

[!OBSERVAçãO] O comportamento padrão do RDS pode ser chamado implicitamente com os objetos ADO e o Microsoft OLE DB Remoting Provider. As consultas podem **** retornar Recordsets, e **** os Recordsets editados podem atualizar a fonte de dados. Esse tutorial não chama o RDS com objetos ADO, mas veja como seria se o fizesse:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a>Parte A 

Para esse caso assuma que você tenha usado apenas [RDS.DataControl](datacontrol-object-rds.md) e que um objeto **Recordset** agora esteja associado ao **RDS.DataControl**. O método [SubmitChanges](submitchanges-method-rds.md) atualiza a origem de dados com todas as alterações ao objeto **Recordset** se as propriedades [Server](server-property-rds.md) e [Connect](connect-property-rds.md) ainda estiverem definidas.

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

### <a name="part-b"></a>Parte B 

Como alternativa, você poderia atualizar o servidor com o objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md), especificando uma conexão e um objeto **Recordset**.

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```


## <a name="appendix-a-rds-tutorial-vbscript"></a>Apêndice A: tutorial RDS (VBScript)

Este é o tutorial do RDS, escrito no Microsoft Visual Basic Scripting Edition. Para obter uma descrição do objetivo deste tutorial, consulte a introdução a este tópico.

Neste tutorial, o [RDS. DataControl](datacontrol-object-rds.md) e [RDS. DataSpace](dataspace-object-rds.md) são criados no tempo de design; ou seja, eles são definidos com marcas de objeto. Como alternativa, eles podem ser criados no momento da execução com o método **Server.CreateObject**. 

Por exemplo, o objeto **RDS.DataControl** pode ser criado dessa forma:

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

### <a name="step-1-specify-a-server-program"></a>Etapa 1: especificar um programa de servidor

O VBScript pode descobrir o nome do servidor Web IIS em que está sendo executado, acessando o método de solicitação do VBScript **. ServerVariables** disponível para Active Server Pages:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

No enTanto, para este tutorial, use o servidor imaginário, "yourServer".

> [!NOTE]
> [!OBSERVAçãO] Preste atenção nos tipos de dados dos argumentos **ByRef**. O VBScript não permite que você especifique o tipo de variável, então, você deve sempre transmitir uma Variant. Quando HTTP for utilizado, o RDS permitirá a transmissão de uma Variant para um método que espera uma non-Variant, se você chamá-lo com o método **CreateObject** do objeto [RDS.DataSpace](createobject-method-rds.md). Ao utilizar DCOM ou um servidor em execução, corresponda os tipos de parâmetros no cliente e no servidor; caso contrário, receberá um erro "Incompatibilidade de tipo".

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a>Etapa 2, parte A: invocar o programa do servidor com RDS. DataControl

Esse exemplo é meramente um comentário para demonstrar que o comportamento padrão do **RDS.DataControl** destina-se a executar a consulta especificada.

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

Pule para a etapa a seguir.

### <a name="step-4-server-returns-the-recordset"></a>Etapa 4: o servidor retorna o Recordset

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a>Etapa 5: o dataControl é tornado utilizável por controles visuais

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a>Etapa 6, parte A: as alterações são enviadas para o servidor com o RDS. DataControl

Esse exemplo é meramente um comentário que demonstra como o **RDS.DataControl** executa as atualizações.

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>Etapa 6, parte B: as alterações são enviadas para o servidor com o RDSServer. dataFactory

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a>Apêndice B: tutorial do RDS (Visual J++)

O ADO/WFC não segue completamente o modelo de objeto RDS porque não implementa o objeto [RDS.DataControl](datacontrol-object-rds.md). O ADO/WFC apenas implementa a classe do lado do cliente, [RDS.DataSpace](dataspace-object-rds.md).

A classe **DataSpace** implementa um método, [CreateObject](createobject-method-rds.md), que retorna um objeto [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax). A classe **DataSpace** também implementa a propriedade [InternetTimeout](internettimeout-property-rds.md).

A classe **ObjectProxy** implementa um método, call, que pode chamar qualquer objeto de negócios do lado do servidor.

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



