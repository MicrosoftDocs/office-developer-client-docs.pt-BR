---
<<<<<<< Título cabeça: propriedade Rowset (ADO) TOCTitle: propriedade Rowset (ADO) === título: propriedade Rowset (ADO) TOCTitle: propriedade Rowset (ADO)
>>>>>>> ms:assetid de mestre: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: ms.date 48543515: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="rowset-property-ado"></a>Propriedade Rowset (ADO)
=======
# <a name="rowset-property-ado"></a>Propriedade RowSet (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013



Obtém ou define um objeto **Rowset** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**. Quando você usa put\_Rowset, o conjunto de linhas seja transformado em um objeto **Recordset** do ADO.

Leitura/gravação.

## <a name="syntax"></a>Sintaxe

Get HRESULT\_Rowset (\[check-out, retval\] IUnknown\* \* ppRowset);

Colocar HRESULT\_Rowset (\[na\] IUnknown\* pRowset);

## <a name="parameters"></a>Parâmetros

  - *ppRowset*

  - Ponteiro para um objeto **Rowset** do OLE DB.

  - *PRowset*

  - Um objeto **Rowset** do OLE DB.

<<<<<<< Cabeça
## <a name="return-values"></a>Valores de retorno
=======
## <a name="return-values"></a>Valor de retorno
>>>>>>> mestre

Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.

## <a name="applies-to"></a>Aplica-se a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

