---
<<<<<<< Título cabeça: propriedade AbsolutePosition (ADO) TOCTitle: ms:assetid propriedade AbsolutePosition (ADO): 500be001-9fa1-177b-f19d-acf003a0cdc2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15) ms:contentKeyID: ms.date 48544787: mtps_ 18/09/2015 versão: v=office.15
---

# <a name="absoluteposition-property-ado"></a>Propriedade AbsolutePosition (ADO)

=== título: a propriedade AbsolutePosition (ADO) TOCTitle: ms:assetid de propriedade (ADO) AbsolutePosition: 500be001-9fa1-177b-f19d-acf003a0cdc2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15) ms:contentKeyID: ms.date 48544787: 10/17/2018 mtps_version: v=office.15
---

# <a name="absoluteposition-property-ado"></a>Propriedade AbsolutePosition (ADO)
>>>>>>> mestre

**Aplica-se a**: Access 2013 | Office 2013

Indica a posição ordinal do registro atual de um objeto [Recordset](recordset-object-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **Long** de 1 até o número de registros no objeto **Recordset**  ([RecordCount](recordcount-property-ado.md)) ou retorna um dos valores [PositionEnum](positionenum.md).

## <a name="remarks"></a>Comentários

<<<<<<< Cabeça na ordem para definir a propriedade **AbsolutePosition** , o ADO requer que o provedor OLE DB que você estiver usando implementar a interface IRowsetLocate.
=== Para definir a propriedade **AbsolutePosition** , o ADO requer que o provedor OLE DB que você estiver usando implementar a interface IRowsetLocate.
>>>>>>> mestre

O acesso à propriedade **AbsolutePosition** de um **Recordset** aberto usando um cursor somente de encaminhamento ou dinâmico provoca o erro **adErrFeatureNotAvailable**. Com outros tipos de cursor, a posição correta será retornada, desde que o provedor ofereça suporte à interface IRowsetScroll. Se o provedor não oferecer suporte a essa *interface*, a propriedade será definida como **adPosUnknown**. Consulte a documentação do seu provedor para identificar se ele oferece suporte à *IRowsetScroll*.

Use a propriedade **AbsolutePosition** para mover um registro, de acordo com sua posição ordinal no objeto **Recordset** ou para determinar a posição ordinal do registro atual. O provedor deve oferecer suporte à funcionalidade apropriada para que essa propriedade esteja disponível.

Assim como a propriedade [AbsolutePage](absolutepage-property-ado.md), **AbsolutePosition** tem base unitária e equivale a 1 quando o registro atual é o primeiro registro no **Recordset**. É possível obter o número total de registros no objeto **Recordset** usando a propriedade [RecordCount](recordcount-property-ado.md).

<<<<<<< Cabeça quando você definir a propriedade **AbsolutePosition** , mesmo se ele for para um registro em memória cache atual, o ADO recarrega o cache com um novo grupo de registros que começam com o registro que você especificou. A propriedade [CacheSize](cachesize-property-ado.md) determina o tamanho desse grupo.


> [!NOTE]
> <a name="pyou-should-not-use-the-strongabsolutepositionstrong-property-as-a-surrogate-record-number-the-position-of-a-given-record-changes-when-you-delete-a-preceding-record-there-is-also-no-assurance-that-a-given-record-will-have-the-same-strongabsolutepositionstrong-if-the-strongrecordsetstrong-object-is-requeried-or-reopened-bookmarks-are-still-the-recommended-way-of-retaining-and-returning-to-a-given-position-and-are-the-only-way-of-positioning-across-all-types-of-strongrecordsetstrong-objectsp"></a><P>[!OBSERVAçãO] Não se deve usar a propriedade <STRONG>AbsolutePosition</STRONG> como um número de registro substituto. A posição de um determinado registro é alterada quando um registro precedente é excluído. Também não há garantias de que um determinado registro terá a mesma <STRONG>AbsolutePosition</STRONG> se o objeto <STRONG>Recordset</STRONG> for consultado e aberto novamente. Os indicadores ainda são o modo recomendado para se reter e retornar a uma determinada posição e são o único modo de posicionamento presente em todos os tipos de objetos <STRONG>Recordset</STRONG>.</P>
=======
Quando você define a propriedade **AbsolutePosition** , mesmo se ele for para um registro em memória cache atual, o ADO recarrega o cache com um novo grupo de registros que começam com o registro que você especificou. A propriedade [CacheSize](cachesize-property-ado.md) determina o tamanho desse grupo.


> [!NOTE]
> [!OBSERVAçãO] A propriedade **AbsolutePosition** não deve ser usada como um número de registro substituto. A posição de um determinado registro é alterada quando um registro precedente é excluído. Também não há garantias de que um determinado registro terá a mesma **AbsolutePosition** se o objeto **Recordset** for consultado e aberto novamente. Indicadores ainda são a maneira recomendada de reter e retornar para uma determinada posição e são a única maneira de posicionamento em todos os tipos de objetos **Recordset** .
>>>>>>> mestre


