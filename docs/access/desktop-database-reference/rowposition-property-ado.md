---
<<<<<<< Título cabeça: propriedade RowPosition (ADO) TOCTitle: propriedade RowPosition (ADO) === título: propriedade RowPosition (ADO) TOCTitle: propriedade RowPosition (ADO)
>>>>>>> ms:assetid de mestre: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: ms.date 48547325: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="rowposition-property-ado"></a>Propriedade RowPosition (ADO)
=======
# <a name="rowposition-property-ado"></a>Propriedade RowPosition (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013



Obtém ou define um objeto **RowPosition** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**. Quando você usa **colocar\_RowPosition** para definir o objeto **RowPosition** , o objeto **Recordset** resultante usa o objeto **RowPosition** para determinar a linha atual.

Leitura/gravação.

## <a name="syntax"></a>Sintaxe

Get HRESULT\_RowPosition (\[check-out, retval\] IUnknown\* \* ppRowPos);

Colocar HRESULT\_RowPosition (\[na\] IUnknown\* pRowPos);

## <a name="parameters"></a>Parâmetros

  - *ppRowPos*

  - Ponteiro para um objeto **RowPosition** do OLE DB.

  - *PRowPos*

  - Um objeto **RowPosition** do OLE DB.

<<<<<<< Cabeça
## <a name="return-values"></a>Valores de retorno
=======
## <a name="return-values"></a>Valor de retorno
>>>>>>> mestre

Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.

## <a name="remarks"></a>Comentários

Quando esta propriedade for definida, se o objeto **Rowset** no objeto **RowPosition** for diferente do objeto **Rowset** no objeto **Recordset**, o primeiro substituirá o segundo. O mesmo comportamento também se aplicará ao **Charter** atual do **RowPosition**.

## <a name="applies-to"></a>Aplica-se a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

