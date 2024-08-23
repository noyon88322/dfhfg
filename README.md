## একটা ক্যাটাগরির আন্ডারে একের পর এক ডাটা সাজাবো

# Like

![Screenshot (4)](https://github.com/user-attachments/assets/07c353c3-2814-4df8-88b5-4faaf499b7e2)



   ```bash


                catRef = FirebaseDatabase.getInstance().getReference("Categorise");
                HashMap hashMap = new HashMap();
                hashMap.put("title",categoryName);

//                Toast.makeText(AddCategoryActivity.this, ""+categoryName, Toast.LENGTH_SHORT).show();

                catRef.child(categoryName).setValue(hashMap).addOnCompleteListener(new OnCompleteListener<Void>() {
                    @Override
                    public void onComplete(@NonNull Task<Void> task) {
                        if (task.isSuccessful()){
                            Toast.makeText(AddCategoryActivity.this, "Successfully", Toast.LENGTH_SHORT).show();
                        }
                    }
                });

   ```
