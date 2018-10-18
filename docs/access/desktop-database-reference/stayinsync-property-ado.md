---
<<<<<<< Título cabeça: propriedade StayInSync (ADO) TOCTitle: propriedade StayInSync (ADO) === título: propriedade StayInSync (ADO) TOCTitle: propriedade StayInSync (ADO)
>>>>>>> ms:assetid de mestre: 02c95c10-4032-14e1-e506-f334a8787142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15) ms:contentKeyID: ms.date 48542966: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="stayinsync-property-ado"></a>Propriedade StayInSync (ADO)
=======
# <a name="stayinsync-property-ado"></a>Propriedade StayInSync (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica, em um objeto [Recordset](recordset-object-ado.md) hierárquico, se a referência a registros filhos de base (isto é, o *capítulo*) é alterada quando a posição da linha pai é alterada.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **Boolean**. O valor padrão é **True**. Se for **True**, o capítulo será atualizado se o objeto pai **Recordset** alterar a posição da linha; se for **False**, o capítulo continuará a fazer referência aos dados do capítulo anterior, ainda que o objeto pai **Recordset** tenha alterado a posição da linha.

## <a name="remarks"></a>Comentários

Essa propriedade aplica-se aos Recordsets hierárquicos, como aqueles que contam com suporte do [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), e deve ser definida no **Recordset** pai antes que o **Recordset** filho seja recuperado. Essa propriedade simplifica a navegação pelos conjuntos de registros hierárquicos.

