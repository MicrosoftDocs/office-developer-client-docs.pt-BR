---
<<<<<<< Título cabeça: HelpContext, HelpFile propriedades (ADO) TOCTitle: HelpContext, HelpFile propriedades (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: ms.date 48546194: 09/18 / 2015 mtps_version: v=office.15
---

# <a name="helpcontext-helpfile-properties-ado"></a>Propriedades HelpContext, HelpFile (ADO)

=== título: Propriedades HelpContext, HelpFile (ADO) TOCTitle: HelpContext, HelpFile propriedades (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: ms.date 48546194: 10/17/2018 mtps_version: v=office.15
---

# <a name="helpcontext-helpfile-properties-ado"></a>Propriedades HelpContext, HelpFile (ADO)
>>>>>>> mestre

**Aplica-se a**: Access 2013 | Office 2013

Indica o arquivo de ajuda e o tópico associado a um objeto [Error](error-object-ado.md).

<<<<<<< Cabeça
## <a name="return-values"></a>Valores de retorno

  - **HelpContextID**  retorna uma ID de contexto, como um valor **Long**, para um tópico em um arquivo de Ajuda.

  - **HelpFile**  retorna um valor **String** que avalia um caminho completamente resolvido para um arquivo de Ajuda.
=======
## <a name="return-values"></a>Valor de retorno

- **HelpContextID**  retorna uma ID de contexto, como um valor **Long**, para um tópico em um arquivo de Ajuda.

- **HelpFile**  retorna um valor **String** que avalia um caminho completamente resolvido para um arquivo de Ajuda.
>>>>>>> mestre

## <a name="remarks"></a>Comentários

Se um arquivo de Ajuda for especificado na propriedade **HelpFile**, a propriedade **HelpContext** será usada para exibir automaticamente o tópico de Ajuda que ela identificar. Se não houver um tópico de ajuda relevante disponível, a propriedade **HelpContext** retornará zero e a propriedade **HelpFile** retornará uma sequência de comprimento zero ("").

