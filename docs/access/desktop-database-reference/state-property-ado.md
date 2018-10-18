---
<<<<<<< Título cabeça: estado Property (ADO) TOCTitle: estado Property (ADO) === título: (ADO) da propriedade State TOCTitle: estado de propriedade (ADO)
>>>>>>> ms:assetid de mestre: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: ms.date 48547053: 18/09/2015 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231176 f1_categories:
- Office.Version=v15
---

<<<<<<< Cabeça
# <a name="state-property-ado"></a>Propriedade State (ADO)
=======
# <a name="state-property-ado"></a>Propriedade State (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica todos os objetos aplicáveis, independentemente de seu estado: aberto ou fechado.

Indica todos os objetos aplicáveis que executam um método assíncrono, independentemente de seu estado atual: conexão, execução ou recuperação.

<<<<<<< Cabeça
## <a name="return-value"></a>Valor retornado
=======
## <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

Retorna um valor **Long** que pode ser um valor [ObjectStateEnum](objectstateenum.md). O valor padrão é **adStateClosed**.

## <a name="remarks"></a>Comentários

Você pode utilizar a propriedade **State** para identificar o estado atual de um determinado objeto em qualquer momento.

A propriedade **State** do objeto pode ter uma combinação de valores. Por exemplo, se uma instrução estiver sendo executada, essa propriedade terá uma combinação de valores de **adStateOpen** e **adStateExecuting**.

A propriedade **State** é somente leitura.

