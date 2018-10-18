---
título: propriedade Row - ActiveX Data Objects (ADO) <<<<<<< TOCTitle cabeça: propriedade de linha (ADO) === TOCTitle: linha de propriedade (ADO)
>>>>>>> ms:assetid de mestre: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: ms.date 48543562: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="row-property-ado"></a>Propriedade Row (ADO)
=======
# <a name="row-property-ado"></a>Propriedade Row (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013



Obtém ou define um objeto **Row** do OLE DB a partir de/em um objeto **ADORecordConstruction**. Quando você usa **colocar\_linha** para definir um objeto **Row** , uma linha seja transformada em um objeto **Record** do ADO. Leitura/gravação.

## <a name="syntax"></a>Sintaxe

Get HRESULT\_linha (\[check-out, retval\] IUnknown\* \* ppRow);

Colocar HRESULT\_linha (\[na\] IUnknown\* pRow);

## <a name="parameters"></a>Parâmetros

  - *ppRow*

  - Ponteiro para um objeto **Row** do OLE DB.

  - *PRow*

  - Um objeto **Row** do OLE DB.

<<<<<<< Cabeça
## <a name="return-values"></a>Valores de retorno
=======
## <a name="return-values"></a>Valor de retorno
>>>>>>> mestre

Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.

## <a name="applies-to"></a>Aplica-se a

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

