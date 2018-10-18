---
<<<<<<< Título cabeça: propriedade CommandTimeout (ADO) TOCTitle: propriedade CommandTimeout (ADO) === título: a propriedade CommandTimeout (ADO) TOCTitle: a propriedade CommandTimeout (ADO)
>>>>>>> ms:assetid de mestre: a0b6209c-9feb-08ae-002a-15d1d20734a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15) ms:contentKeyID: ms.date 48546714: 18/09/2015 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231124 f1_categories:
- Office.Version=v15
---

<<<<<<< Cabeça
# <a name="commandtimeout-property-ado"></a>Propriedade CommandTimeout (ADO)
=======
# <a name="commandtimeout-property-ado"></a>Propriedade CommandTimeout (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica quanto tempo esperar durante a execução de um comando antes de interromper a tentativa e gerar um erro.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **Long** que indica, em segundos, quanto tempo esperar para que um comando seja executado. O padrão é 30.

## <a name="remarks"></a>Comentários

<<<<<<< Cabeça Use a propriedade **CommandTimeout** em um objeto de [Conexão](connection-object-ado.md) ou um objeto [Command](command-object-ado.md) para permitir o cancelamento de uma chamada do método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) , devido a atrasos de rede pesada ou tráfego de uso do servidor. Se o intervalo definido na propriedade **CommandTimeout** terminar antes de o comando concluir a execução, um erro será gerado e o ADO cancelará o comando. Se você definir a propriedade como zero, o ADO aguardará indefinidamente até que a execução seja concluída. Verifique se o provedor e a fonte de dados na qual está escrevendo o código oferecem suporte à funcionalidade **CommandTimeout**.
=== Use a propriedade **CommandTimeout** em um objeto de [Conexão](connection-object-ado.md) ou um objeto [Command](command-object-ado.md) para permitir o cancelamento de uma chamada do método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) , devido a atrasos de rede pesada ou tráfego de uso do servidor. Se o intervalo definido na propriedade **CommandTimeout** terminar antes de o comando concluir a execução, um erro será gerado e o ADO cancelará o comando. Se você definir a propriedade como zero, o ADO aguardará indefinidamente até que a execução seja concluída. Verifique se o provedor e a fonte de dados na qual está escrevendo o código oferecem suporte à funcionalidade **CommandTimeout**.
>>>>>>> mestre

A definição de **CommandTimeout** em um objeto **Connection** não afeta a definição de **CommandTimeout** em um objeto **Command** no mesmo objeto **Connection**; isto é, a propriedade **CommandTimeout** do objeto **Command** não herda o valor de **CommandTimeout** do objeto **Connection**.

Em um objeto **Connection**, a propriedade **CommandTimeout** continua sendo de leitura/gravação depois que **Connection** é aberto.

