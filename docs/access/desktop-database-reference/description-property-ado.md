---
<<<<<<< Título cabeça: propriedade Descrição (ADO) TOCTitle: propriedade Descrição (ADO) === título: a propriedade Description (ADO) TOCTitle: a propriedade Description (ADO)
>>>>>>> ms:assetid de mestre: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: ms.date 48544064: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="description-property-ado"></a>Propriedade Description (ADO)
=======
# <a name="description-property-ado"></a>Propriedade Description (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Descreve um objeto [Error](error-object-ado.md).

<<<<<<< Cabeça
## <a name="return-value"></a>Valor retornado
=======
## <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

Retorna um valor **String** contendo uma descrição do erro.

## <a name="remarks"></a>Comentários

Use a propriedade **Description** para obter uma breve descrição do erro. Exiba essa propriedade para alertar o usuário sobre um erro que você não pode ou não deseja resolver. A sequência virá do ADO ou de um provedor.

Os provedores são responsáveis por passar textos de erro específicos para o ADO. O ADO adiciona um objeto [Error](error-object-ado.md) à coleção **Errors** a cada erro de provedor ou alerta que recebe. Enumere a coleção **Errors** para rastrear os erros que são passados pelo provedor.

