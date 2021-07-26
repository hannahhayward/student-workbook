# What is the difference between a primary key and a foreign key
>a foreign key is a key that will be used from another table while the primary key is the main identifier.
# What is an Alias?
>an alias is another variable for a certain object to make using and setting that object simpler.
# Demonstrate how you would query a join statement that would get all of a doctors patients from the following collections:
# CREATE TABLE doctors (
  # id INT NOT NULL AUTO_INCREMENT,
  # -- CODE OMITTED
  # PRIMARY KEY (id)
# )

# CREATE TABLE patients (
#   id INT NOT NULL AUTO_INCREMENT,
 # -- CODE OMITTED
 # PRIMARY KEY (id)
# )

# CREATE TABLE doctorspatients (
  # id INT NOT NULL AUTO_INCREMENT,
  # doctorId INT NOT NULL,
 #  patientId INT NOT NULL,

  # FOREIGN KEY (doctorId)
   #  REFERENCES doctors(id),
  # FOREIGN KEY (patientId)
   #  REFERENCES patients(id),
# )
>{
      string sql = @"
      SELECT 
      d.*,
      dp.*,
      p.*
      FROM patients p
      JOIN doctorspatients dp ON p.id = dp.patientId
      JOIN doctors d ON d.id = dp.doctorId
      WHERE dp.doctorId = @id;";
      return _db.Query<doctorspatients, Patient, doctorspatients>(sql, (k,vk,p)=>
      {
        dp.pataient = p;
        return dp;
      },new { id }, splitOn: "id").ToList();
    }

    lab link: "https://github.com/hannahhayward/angieslist"
