# Custom fildable regions in VSCode

Sometime you may want to create a custom foldable section in ypur code eg. wrap class methods. We can use the `//#region` tags in vscode

```javascript
//#region Give the region a name and description
React.useEffect(() => {
    getOrderCount({variables: {id: sellerId}})
    setLastFetched(new Date())
  }, [data])

  if (error) {
    return <Alert severity="error">{i18n.t("graphqlError")}</Alert>
  }

  const refresh = useCallback(() => {
    refetch()
    setLastFetched(new Date())
  }, [refetch, setLastFetched]
  //#endregion
```