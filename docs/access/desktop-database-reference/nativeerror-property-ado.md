---
<<<<<<< Título cabeça: propriedade NativeError (ADO) TOCTitle: propriedade NativeError (ADO) === título: propriedade NativeError (ADO) TOCTitle: propriedade NativeError (ADO)
>>>>>>> ms:assetid de mestre: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID: ms.date 48546685: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="nativeerror-property-ado"></a>Propriedade NativeError (ADO)
=======
# <a name="nativeerror-property-ado"></a>Propriedade NativeError (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o código de erro específico do provedor para um determinado objeto [Error](error-object-ado.md).

<<<<<<< Cabeça
## <a name="return-value"></a>Valor retornado
=======
## <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

Retorna um valor **Long** que indica o código de erro.

## <a name="remarks"></a>Comentários

Use a propriedade **NativeError** para recuperar as informações de erro específicas do banco de dados para um determinado objeto **Error**. Por exemplo, ao usar o Microsoft ODBC Provider para OLE DB com um banco de dados Microsoft SQL Server, os códigos de erro nativos originados do SQL Server passam pelo ODBC e ODBC Provider para a propriedade **NativeError** do ADO.

