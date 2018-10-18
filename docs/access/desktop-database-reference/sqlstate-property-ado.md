---
<<<<<<< Título cabeça: propriedade SQLState (ADO) TOCTitle: propriedade SQLState (ADO) === título: propriedade SQLState (ADO) TOCTitle: propriedade SQLState (ADO)
>>>>>>> ms:assetid de mestre: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: ms.date 48547806: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="sqlstate-property-ado"></a>Propriedade SQLState (ADO)
=======
# <a name="sqlstate-property-ado"></a>Propriedade SQLState (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o estado do SQL de um determinado objeto [Error](error-object-ado.md).

<<<<<<< Cabeça
## <a name="return-value"></a>Valor retornado
=======
## <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

Retorna um valor **String** de cinco caracteres que segue o padrão ANSI SQL e indica o código de erro.

## <a name="remarks"></a>Comentários

Utilize a propriedade **SQLState** para ler o código de erro de cinco caracteres que o provedor retornar quando ocorrer um erro durante o processamento de uma instrução SQL. Por exemplo, ao utillizar o Microsoft OLE DB Provider for ODBC com um banco de dados Microsoft SQL Server, os códigos de erro do estado do SQL serão originados do ODBC, com base nos erros específicos para o ODBC, ou em erros que se originaram do Microsoft SQL Server e, em seguida, serão mapeados para os erros do ODBC. Esses códigos de erro são documentados no padrão ANSI SQL, mas poderão ser implementados de formas diferentes por diversas fontes de dados.

