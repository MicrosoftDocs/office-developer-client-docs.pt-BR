---
<<<<<<< Título cabeça: propriedade CommandText (ADO) TOCTitle: propriedade CommandText (ADO) === título: a propriedade CommandText (ADO) TOCTitle: a propriedade CommandText (ADO)
>>>>>>> ms:assetid de mestre: 0debec1c-068f-0aea-fce8-e61aa39c5907 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15) ms:contentKeyID: ms.date 48543234: 18/09/2015 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231123 f1_categories:
- Office.Version=v15
---

<<<<<<< Cabeça
# <a name="commandtext-property-ado"></a>Propriedade CommandText (ADO)
=======
# <a name="commandtext-property-ado"></a>Propriedade CommandText (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o texto de um comando a ser emitido para um provedor.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **String** contendo um comando de provedor, como uma instrução SQL, um nome de tabela, uma URL relativa ou uma chamada de procedimento armazenado. O padrão é "" (sequência de comprimento zero).

## <a name="remarks"></a>Comentários

Use a propriedade **CommandText** para definir ou retornar o texto de um comando representado por um objeto [Command](command-object-ado.md). Geralmente, é uma instrução SQL, mas também pode ser qualquer outro tipo de instrução de comando reconhecida pelo provedor, como uma chamada de procedimento armazenado. Uma instrução SQL deve ser de um dialeto ou versão específica que tenha suporte do processador de consultas do provedor.

<<<<<<< Cabeça se a propriedade [preparada](prepared-property-ado.md) do objeto **Command** é definida como **True** e o objeto **Command** é acoplado a uma conexão aberta quando você definir a propriedade **CommandText** , ADO prepara o (de consulta ou seja, um formulário compilado da consulta é armazenado pelo provedor) quando você chama os métodos [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) ou **Open** .
=== Se a propriedade [preparada](prepared-property-ado.md) do objeto **Command** é definida como **True** e o objeto **Command** é acoplado a uma conexão aberta quando você definir a propriedade **CommandText** , ADO prepara a consulta (ou seja, uma forma compilada do consulta que é armazenada pelo provedor) quando você chama os métodos [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) ou **Open** .
>>>>>>> mestre

Dependendo da definição da propriedade [CommandType](commandtype-property-ado.md), o ADO poderá alterar a propriedade **CommandText**. Você pode ler a propriedade **CommandText** a qualquer momento para ver o texto de comando real que será utilizado pelo ADO durante a execução.

Use a propriedade **CommandText** para definir ou retornar uma URL relativa que especifique um recurso, como um arquivo ou um diretório. O recurso é relativo a um local especificado explicitamente por uma URL absoluta ou implicitamente por um objeto [Connection](connection-object-ado.md) aberto.


> [!NOTE]
<<<<<<< Cabeça
> <P>[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs Absolutas e Relativas</A>.</P>
=======
> [!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).
>>>>>>> mestre


