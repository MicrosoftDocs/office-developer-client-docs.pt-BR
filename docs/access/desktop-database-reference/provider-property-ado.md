---
<<<<<<< Título cabeça: TOCTitle provedor Property (ADO): propriedade do provedor (ADO) === título: propriedade Provider (ADO) TOCTitle: a propriedade Provider (ADO)
>>>>>>> ms:assetid de mestre: 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID: ms.date 48543543: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="provider-property-ado"></a>Propriedade Provider (ADO)
=======
# <a name="provider-property-ado"></a>Propriedade Provider (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o nome do provedor de um objeto [Connection](connection-object-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **String** que indica o nome do provedor.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Provider** para definir ou retornar o nome do provedor para uma conexão. Essa propriedade também pode ser definida pelo conteúdo da propriedade [ConnectionString](connectionstring-property-ado.md) ou pelo argumento *ConnectionString *  do método [Open](open-method-ado-connection.md); entretanto, a especificação de um provedor em mais de um local enquanto o método **Open** é chamado pode gerar resultados imprevisíveis. Se nenhum provedor for especificado, a propriedade assumirá o padrão de MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).

A propriedade **Provider** é leitura/gravação quando a conexão estiver fechada e somente leitura quando estiver aberta. A definição será efetivada somente após a abertura do objeto **Connection** ou o acesso à coleção [Properties](properties-collection-ado.md) do objeto **Connection**. Haverá erro se a definição não for válida.

