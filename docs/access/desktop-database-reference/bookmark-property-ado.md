---
<<<<<<< Título cabeça: propriedade Bookmark (ADO) TOCTitle: propriedade Bookmark (ADO) === título: propriedade Bookmark (ADO) TOCTitle: propriedade Bookmark (ADO)
>>>>>>> ms:assetid de mestre: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15) ms:contentKeyID: ms.date 48543287: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="bookmark-property-ado"></a>Propriedade Bookmark (ADO)
=======
# <a name="bookmark-property-ado"></a>Propriedade Bookmark (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Aponta um indicador que identifica com exclusividade o registro atual em um objeto [Recordset](recordset-object-ado.md) ou define o registro atual em um objeto **Recordset** para o registro identificado por um indicador válido.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Configura ou retorna uma expressão **Variant** que avalia um indicador válido.

## <a name="remarks"></a>Comentários

Use a propriedade **Bookmark** para salvar a posição do registro atual e retornar para esse registro a qualquer momento. Bookmarks estão disponíveis apenas em objetos **Recordset** que ofereçam suporte à funcionalidade de indicadores.

Quando um objeto **Recordset** é aberto, cada um dos registros tem um indicador exclusivo. Para salvar o indicador do registro atual, atribua o valor da propriedade **Bookmark** a uma variável. Para retornar rapidamente àquele registro depois de se mover para um registro diferente, defina a propriedade **Bookmark** do objeto **Recordset** com o valor daquela variável.

Talvez o usuário não seja capaz de exibir o valor do indicador. Além disso, os usuários não devem esperar que os indicadores sejam comparados diretamente  dois indicadores referentes ao mesmo registro podem ter valores diferentes.

Se você usar o método [Clone](clone-method-ado.md) para criar uma cópia de um objeto **Recordset**, as definições da propriedade **Bookmark** para os objetos **Recordset** original e duplicado serão idênticas e você poderá usá-las alternadamente. Contudo, não é possível usar indicadores de objetos **Recordset** diferentes alternadamente, mesmo que eles tenham sido criados a partir da mesma fonte ou comando.

**Uso de serviço de dados remotos** Quando usado em um objeto **Recordset** do lado do cliente, a propriedade **Bookmark** está sempre disponível.

