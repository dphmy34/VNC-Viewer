# VNC-Viewer

arr_test = []
with open(r"data/ner_test.txt", "r", encoding = "utf-8") as f:
    for line in f:
        if line != "\n":
            arr_test.append(line.split(" ")[0].replace("\ufeff", ""))
        else:
            res = p.predict(arr_test)
            arr_test = []
            
            
 # write file
        with open(r'D:\NER\code\BiLSTM_CNN\results\label_predict_test.txt', 'a') as f:
            for i in pred:
                f.write(str(i)+"\n")
            f.write("\n")
        return list(zip(words,pred))
