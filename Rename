
package main

import (
	"fmt"
	"io/ioutil"
	"strings"

	"os"
	"path/filepath"
)

func main() {
	path := "C:\\Users\\86178\\Pictures\\数据图"
	files, _ := ioutil.ReadDir(path)
	for index, f := range files {
		// 带扩展名的文件名
		fullFilename := f.Name()
		fmt.Println(index,fullFilename)
		//fmt.Println(fullFilename)
		//扩展名
		fileExt := filepath.Ext(f.Name())
		//fmt.Println(fileExt)
		// 不带扩展名的文件名
		filenameOnly := strings.TrimSuffix(fullFilename, fileExt)
		//fmt.Println(filenameOnly)
		//将每个文件名后面加上1，扩展名不变
		//os.Rename(path+"\\"+f.Name(), path+"\\"+fmt.Sprintf("%s%s%s", filenameOnly, "1", fileExt))
		//将每个文件名中的1替换为2，扩展名不变
		os.Rename(path+"\\"+f.Name(), path+"\\"+fmt.Sprintf("%s%s", strings.Replace(filenameOnly, "2", "1", 1), fileExt))
		fullFilename = f.Name()
		fmt.Println(index,fullFilename)
		fmt.Println("-------------")
	}
}
