---
<<<<<<< Título cabeça: propriedade CommandType (ADO) TOCTitle: propriedade CommandType (ADO) === título: propriedade CommandType (ADO) TOCTitle: propriedade CommandType (ADO)
>>>>>>> ms:assetid de mestre: c8d4fc1c-502b-11f3-af9d-605a03b6f056 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15) ms:contentKeyID: ms.date 48547663: 18/09/2015 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231125 f1_categories:
- Office.Version=v15
---

<<<<<<< Cabeça
# <a name="commandtype-property-ado"></a>Propriedade CommandType (ADO)
=======
# <a name="commandtype-property-ado"></a>Propriedade CommandType (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o tipo de um objeto [Command](command-object-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um ou mais valores [CommandTypeEnum](commandtypeenum.md).


> [!NOTE]
> <P>[!OBSERVAçãO] Não use valores <STRONG>CommandTypeEnum</STRONG> de <STRONG>adCmdFile</STRONG> ou <STRONG>adCmdTableDirect</STRONG> com <STRONG>CommandType</STRONG>. Esses valores podem ser usados somente como opções com os métodos <A href="open-method-ado-recordset.md">Open</A> e <A href="requery-method-ado.md">Requery</A> de um <A href="recordset-object-ado.md">Recordset</A>.</P>



## <a name="remarks"></a>Comentários

Use a propriedade **CommandType** para otimizar a avaliação da propriedade [CommandText](commandtext-property-ado.md).

<<<<<<< Cabeça se o valor da propriedade **CommandType** for igual a **adCmdUnknown** (o valor padrão), você pode enfrentar diminuição do desempenho, pois ADO deve fazer chamadas para o provedor para determinar se o **CommandText** propriedade é uma instrução SQL, um procedimento armazenado ou um nome de tabela. Se você souber que tipo de comando está usando, definir a propriedade **CommandType** instrui o ADO a ir diretamente para o código relevante. Se a propriedade **CommandType** não corresponder ao tipo de comando na propriedade **CommandText**, ocorrerá um erro quando você chamar o método [Open](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).
=== Se o valor da propriedade **CommandType** for igual a **adCmdUnknown** (o valor padrão), você pode enfrentar diminuição do desempenho porque ADO deve fazer chamadas para o provedor para determinar se a propriedade **CommandText** é uma instrução SQL, um procedimento armazenado ou um nome de tabela. Se você souber que tipo de comando está usando, definir a propriedade **CommandType** instrui o ADO a ir diretamente para o código relevante. Se a propriedade **CommandType** não corresponder ao tipo de comando na propriedade **CommandText**, ocorrerá um erro quando você chamar o método [Open](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).
>>>>>>> mestre

