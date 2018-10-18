---
<<<<<<< Título cabeça: propriedade RecordCount (ADO) TOCTitle: propriedade RecordCount (ADO) === título: a propriedade RecordCount (ADO) TOCTitle: a propriedade RecordCount (ADO)
>>>>>>> ms:assetid de mestre: e3072d10-5bf7-02a8-027e-a9d9a34e3f27 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15) ms:contentKeyID: ms.date 48548304: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="recordcount-property-ado"></a>Propriedade RecordCount (ADO)
=======
# <a name="recordcount-property-ado"></a>Propriedade RecordCount (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o número de registros em um objeto [Recordset](recordset-object-ado.md).

<<<<<<< Cabeça
## <a name="return-value"></a>Valor retornado
=======
## <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

Retorna um valor **Long** que indica o número de registros no **Recordset**.

## <a name="remarks"></a>Comentários

Utilize a propriedade **RecordCount** para saber a quantidade de registros existentes em um objeto **Recordset**. A propriedade retorna -1 quando o ADO não puder determinar o número de registros ou se um tipo de provedor ou cursornão oferecer suporte à **RecordCount**. A leitura da propriedade **RecordCount** em um **Recordset** fechado gera um erro.

Se o objeto **Recordset** oferecer suporte a posicionamento ou indicadores aproximados  isto é, **Supports (adApproxPosition)** ou **Supports (adBookmark)**, respectivamente, ele retornará **True**  este valor será o número exato de registros do **Recordset**, independentemente de ter sido preenchido completamente. Se o objeto **Recordset** não oferecer suporte ao posicionamento aproximado, essa propriedade poderá consumir recursos de forma significativa, pois todos os registros terão que ser recuperados e contados para que um valor preciso de **RecordCount** seja retornado.

O tipo de cursor do objeto **Recordset** será afetado se o número de registros puder ser determinado. A propriedade **RecordCount** retornará -1 para um cursor somente de encaminhamento; a contagem real de um cursor estático ou de conjunto de chaves; e -1 ou a contagem real para um cursor dinâmico, dependendo da fonte de dados.

