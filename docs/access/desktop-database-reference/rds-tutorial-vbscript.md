---
title: Tutorial do RDS (VBScript)
TOCTitle: RDS Tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d8bc6d0bb2b2f5402a10a690bb0003170357b21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463760"
---
# <a name="rds-tutorial-vbscript"></a>Tutorial do RDS (VBScript)


**Aplica-se a**: Access 2013 | Office 2013

Este é um tutorial do RDS, escrito no Microsoft Visual Basic Scripting Edition. Para obter uma descrição do objetivo deste tutorial, consulte [Tutorial do RDS](chapter-12-rds-tutorial.md).

Neste tutorial, [RDS. DataControl](datacontrol-object-rds.md) e [RDS. DataSpace](dataspace-object-rds.md) são criados em tempo de design — ou seja, eles são definidos com marcas de objeto, semelhante a esta:. Como alternativa, eles podem ser criados no momento da execução com o método **Server.CreateObject**. Por exemplo, o objeto **RDS.DataControl** pode ser criado dessa forma:

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

**Etapa 1  Especificar um programa de servidor**

O VBScript pode descobrir o nome do servidor Web IIS em que está sendo executado, acessando o método VBScript **Request.ServerVariables** disponível para Active Server Pages:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Contudo, para esse tutorial, use o servidor imaginário "yourServer".


> [!NOTE]
> <P>[!OBSERVAçãO] Preste atenção nos tipos de dados dos argumentos <STRONG>ByRef</STRONG>. O VBScript não permite que você especifique o tipo de variável, então, você deve sempre transmitir uma Variant. Quando HTTP for utilizado, o RDS permitirá a transmissão de uma Variant para um método que espera uma non-Variant, se você chamá-lo com o método <STRONG>CreateObject</STRONG> do objeto <A href="createobject-method-rds.md">RDS.DataSpace</A>. Ao utilizar DCOM ou um servidor em execução, corresponda os tipos de parâmetros no cliente e no servidor; caso contrário, receberá um erro "Incompatibilidade de tipo".</P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

**Etapa 2a  Chamar o programa do servidor com RDS.DataControl**

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

**Etapa 2a  Chamar o programa do servidor com RDS.DataControl**

**Etapa 3  O servidor obtém um Recordset**

**Etapa 4  O servidor retorna o Recordset**

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

**Etapa 5  O DataControl torna-se disponível por meio de controles visuais**

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

**Etapa 6a  As alterações são enviadas para o servidor com o RDS.DataControl**

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

**Etapa 6b  As alterações são enviadas para o servidor com o RDSServer.DataFactory**

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

**Aqui é o final do tutorial.**
