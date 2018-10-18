---
<<<<<<< Título cabeça: TOCTitle propriedade AbsolutePage (ADO): propriedade AbsolutePage (ADO) ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15) ms:contentKeyID: ms.date 48547288: mtps_version 18/09/2015: v = Office.15
---

# <a name="absolutepage-property-ado"></a>Propriedade AbsolutePage (ADO)

=== título: propriedade AbsolutePage (ADO) TOCTitle: ms:assetid de propriedade (ADO) AbsolutePage: b6e5daac-cc21-0aa6-9119-a973595762bb ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15) ms:contentKeyID: ms.date 48547288: 10/17/2018 mtps_version: v=office.15
---

# <a name="absolutepage-property-ado"></a>Propriedade AbsolutePage (ADO)
>>>>>>> mestre

**Aplica-se a**: Access 2013 | Office 2013

Indica a página na qual está o registro atual.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valores de retorno

<a name="sets-or-returns-a-long-value-from-1-to-the-number-of-pages-in-the-recordsetrecordset-object-adomd-object--pagecountpagecount-property-adomd--or-returns-one-of-the-positionenumpositionenummd-values"></a>Define ou retorna um valor **Long** de 1 até o número de páginas no objeto [Recordset](recordset-object-ado.md) ( [PageCount](pagecount-property-ado.md)) ou retorna um dos valores [PositionEnum](positionenum.md).
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** de 1 até o número de páginas no objeto [Recordset](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) ou retorna um dos valores [PositionEnum](positionenum.md) .
>>>>>>> mestre

## <a name="remarks"></a>Comentários

Essa propriedade pode ser usada para identificar o número da página na qual o registro atual está localizado. Ela usa a propriedade [PageSize](pagesize-property-ado.md) para dividir de modo lógico a contagem total do conjunto de linhas do objeto **Recordset** em uma série de páginas, cada qual com um número de registros equivalente à **PageSize** (exceto a última página, que pode conter um número menor de registros). O provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.

Ao obter ou configurar a propriedade **AbsolutePage**, o ADO usa as propriedades [AbsolutePosition](absoluteposition-property-ado.md) e [PageSize](pagesize-property-ado.md) conjuntamente conforme se segue:

<<<<<<< Cabeça
  - Para obter a **AbsolutePage**, o ADO primeiro recupera a **AbsolutePosition** e a divide pela **PageSize**.

  - Para definir a **AbsolutePage**, o ADO move a **AbsolutePosition** da seguinte maneira: ele multiplica a **PageSize** pelo novo valor da **AbsolutePage** e acrescenta 1 ao valor. Como resultado, a posição atual no **Recordset** após a configuração bem-sucedida da **AbsolutePage** é o primeiro registro daquela página.
=======
- Para obter a **AbsolutePage**, o ADO primeiro recupera a **AbsolutePosition** e a divide pela **PageSize**.

- Para definir a **AbsolutePage**, o ADO move a **AbsolutePosition** da seguinte maneira: ele multiplica a **PageSize** pelo novo valor da **AbsolutePage** e acrescenta 1 ao valor. Como resultado, a posição atual no **Recordset** depois de configurar com êxito a **AbsolutePage** é o primeiro registro nessa página.
>>>>>>> mestre

Da mesma forma que a propriedade **AbsolutePosition**, a **AbsolutePage** tem base unitária e equivale a 1 quando o registro atual é o primeiro registro no **Recordset**. Defina essa propriedade para mover para o primeiro registro de uma página específica. Obtenha o número total de páginas da propriedade **PageCount**.

