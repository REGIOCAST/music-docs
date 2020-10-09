+++
date = "2000-01-01T00:00:00+00:02"
title = "C#"
description = "Generate your SDK with the help of Swagger"
toc = true
+++

Music generates documentation with the help of Swagger. You can use the [swagger-codegen](https://github.com/swagger-api/swagger-codegen) tool from the swagger project to generate:

* RestClient for the HTTP calls
* Newtonsoft.Json for JSON marshalling
* .NET DataContract for the models.

You can either download the [cli app](https://swagger.io/tools/swagger-codegen/download/) or use the [online editor](https://editor.swagger.io/). The Album model look like this:

```csharp
using System;
using System.Linq;
using System.IO;
using System.Text;
using System.Text.RegularExpressions;
using System.Collections;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Runtime.Serialization;
using Newtonsoft.Json;
using Newtonsoft.Json.Converters;
using System.ComponentModel.DataAnnotations;
using SwaggerDateConverter = IO.Swagger.Client.SwaggerDateConverter;

namespace IO.Swagger.Model
{
    /// <summary>
    /// CoreAlbum
    /// </summary>
    [DataContract]
    public partial class CoreAlbum :  IEquatable<CoreAlbum>, IValidatableObject
    {
        /// <summary>
        /// Initializes a new instance of the <see cref="CoreAlbum" /> class.
        /// </summary>
        /// <param name="copyright">The copyright text..</param>
        /// <param name="createdAt">createdAt.</param>
        /// <param name="id">id.</param>
        /// <param name="isComplete">(Required) Indicates whether the album is complete. If true, the album is complete; otherwise, it is not. An album is complete if it contains all its tracks and songs..</param>
        /// <param name="isSingle">(Required) Indicates whether the album contains a single song..</param>
        /// <param name="name">(Required) The localized name of the album..</param>
        /// <param name="recordLabel">(Required) The name of the record label for the album..</param>
        /// <param name="releaseDate">(Required) The release date of the album in YYYY-MM-DD format..</param>
        /// <param name="trackCount">(Required) The number of tracks..</param>
        /// <param name="updatedAt">updatedAt.</param>
        public CoreAlbum(string copyright = default(string), string createdAt = default(string), string id = default(string), bool? isComplete = default(bool?), bool? isSingle = default(bool?), string name = default(string), string recordLabel = default(string), string releaseDate = default(string), int? trackCount = default(int?), string updatedAt = default(string))
        {
            this.Copyright = copyright;
            this.CreatedAt = createdAt;
            this.Id = id;
            this.IsComplete = isComplete;
            this.IsSingle = isSingle;
            this.Name = name;
            this.RecordLabel = recordLabel;
            this.ReleaseDate = releaseDate;
            this.TrackCount = trackCount;
            this.UpdatedAt = updatedAt;
        }
        
        /// <summary>
        /// The copyright text.
        /// </summary>
        /// <value>The copyright text.</value>
        [DataMember(Name="copyright", EmitDefaultValue=false)]
        public string Copyright { get; set; }

        /// <summary>
        /// Gets or Sets CreatedAt
        /// </summary>
        [DataMember(Name="createdAt", EmitDefaultValue=false)]
        public string CreatedAt { get; set; }

        /// <summary>
        /// Gets or Sets Id
        /// </summary>
        [DataMember(Name="id", EmitDefaultValue=false)]
        public string Id { get; set; }

        /// <summary>
        /// (Required) Indicates whether the album is complete. If true, the album is complete; otherwise, it is not. An album is complete if it contains all its tracks and songs.
        /// </summary>
        /// <value>(Required) Indicates whether the album is complete. If true, the album is complete; otherwise, it is not. An album is complete if it contains all its tracks and songs.</value>
        [DataMember(Name="isComplete", EmitDefaultValue=false)]
        public bool? IsComplete { get; set; }

        /// <summary>
        /// (Required) Indicates whether the album contains a single song.
        /// </summary>
        /// <value>(Required) Indicates whether the album contains a single song.</value>
        [DataMember(Name="isSingle", EmitDefaultValue=false)]
        public bool? IsSingle { get; set; }

        /// <summary>
        /// (Required) The localized name of the album.
        /// </summary>
        /// <value>(Required) The localized name of the album.</value>
        [DataMember(Name="name", EmitDefaultValue=false)]
        public string Name { get; set; }

        /// <summary>
        /// (Required) The name of the record label for the album.
        /// </summary>
        /// <value>(Required) The name of the record label for the album.</value>
        [DataMember(Name="recordLabel", EmitDefaultValue=false)]
        public string RecordLabel { get; set; }

        /// <summary>
        /// (Required) The release date of the album in YYYY-MM-DD format.
        /// </summary>
        /// <value>(Required) The release date of the album in YYYY-MM-DD format.</value>
        [DataMember(Name="releaseDate", EmitDefaultValue=false)]
        public string ReleaseDate { get; set; }

        /// <summary>
        /// (Required) The number of tracks.
        /// </summary>
        /// <value>(Required) The number of tracks.</value>
        [DataMember(Name="trackCount", EmitDefaultValue=false)]
        public int? TrackCount { get; set; }

        /// <summary>
        /// Gets or Sets UpdatedAt
        /// </summary>
        [DataMember(Name="updatedAt", EmitDefaultValue=false)]
        public string UpdatedAt { get; set; }

        /// <summary>
        /// Returns the string presentation of the object
        /// </summary>
        /// <returns>String presentation of the object</returns>
        public override string ToString()
        {
            var sb = new StringBuilder();
            sb.Append("class CoreAlbum {\n");
            sb.Append("  Copyright: ").Append(Copyright).Append("\n");
            sb.Append("  CreatedAt: ").Append(CreatedAt).Append("\n");
            sb.Append("  Id: ").Append(Id).Append("\n");
            sb.Append("  IsComplete: ").Append(IsComplete).Append("\n");
            sb.Append("  IsSingle: ").Append(IsSingle).Append("\n");
            sb.Append("  Name: ").Append(Name).Append("\n");
            sb.Append("  RecordLabel: ").Append(RecordLabel).Append("\n");
            sb.Append("  ReleaseDate: ").Append(ReleaseDate).Append("\n");
            sb.Append("  TrackCount: ").Append(TrackCount).Append("\n");
            sb.Append("  UpdatedAt: ").Append(UpdatedAt).Append("\n");
            sb.Append("}\n");
            return sb.ToString();
        }
  
        /// <summary>
        /// Returns the JSON string presentation of the object
        /// </summary>
        /// <returns>JSON string presentation of the object</returns>
        public virtual string ToJson()
        {
            return JsonConvert.SerializeObject(this, Formatting.Indented);
        }

        /// <summary>
        /// Returns true if objects are equal
        /// </summary>
        /// <param name="input">Object to be compared</param>
        /// <returns>Boolean</returns>
        public override bool Equals(object input)
        {
            return this.Equals(input as CoreAlbum);
        }

        /// <summary>
        /// Returns true if CoreAlbum instances are equal
        /// </summary>
        /// <param name="input">Instance of CoreAlbum to be compared</param>
        /// <returns>Boolean</returns>
        public bool Equals(CoreAlbum input)
        {
            if (input == null)
                return false;

            return 
                (
                    this.Copyright == input.Copyright ||
                    (this.Copyright != null &&
                    this.Copyright.Equals(input.Copyright))
                ) && 
                (
                    this.CreatedAt == input.CreatedAt ||
                    (this.CreatedAt != null &&
                    this.CreatedAt.Equals(input.CreatedAt))
                ) && 
                (
                    this.Id == input.Id ||
                    (this.Id != null &&
                    this.Id.Equals(input.Id))
                ) && 
                (
                    this.IsComplete == input.IsComplete ||
                    (this.IsComplete != null &&
                    this.IsComplete.Equals(input.IsComplete))
                ) && 
                (
                    this.IsSingle == input.IsSingle ||
                    (this.IsSingle != null &&
                    this.IsSingle.Equals(input.IsSingle))
                ) && 
                (
                    this.Name == input.Name ||
                    (this.Name != null &&
                    this.Name.Equals(input.Name))
                ) && 
                (
                    this.RecordLabel == input.RecordLabel ||
                    (this.RecordLabel != null &&
                    this.RecordLabel.Equals(input.RecordLabel))
                ) && 
                (
                    this.ReleaseDate == input.ReleaseDate ||
                    (this.ReleaseDate != null &&
                    this.ReleaseDate.Equals(input.ReleaseDate))
                ) && 
                (
                    this.TrackCount == input.TrackCount ||
                    (this.TrackCount != null &&
                    this.TrackCount.Equals(input.TrackCount))
                ) && 
                (
                    this.UpdatedAt == input.UpdatedAt ||
                    (this.UpdatedAt != null &&
                    this.UpdatedAt.Equals(input.UpdatedAt))
                );
        }

        /// <summary>
        /// Gets the hash code
        /// </summary>
        /// <returns>Hash code</returns>
        public override int GetHashCode()
        {
            unchecked // Overflow is fine, just wrap
            {
                int hashCode = 41;
                if (this.Copyright != null)
                    hashCode = hashCode * 59 + this.Copyright.GetHashCode();
                if (this.CreatedAt != null)
                    hashCode = hashCode * 59 + this.CreatedAt.GetHashCode();
                if (this.Id != null)
                    hashCode = hashCode * 59 + this.Id.GetHashCode();
                if (this.IsComplete != null)
                    hashCode = hashCode * 59 + this.IsComplete.GetHashCode();
                if (this.IsSingle != null)
                    hashCode = hashCode * 59 + this.IsSingle.GetHashCode();
                if (this.Name != null)
                    hashCode = hashCode * 59 + this.Name.GetHashCode();
                if (this.RecordLabel != null)
                    hashCode = hashCode * 59 + this.RecordLabel.GetHashCode();
                if (this.ReleaseDate != null)
                    hashCode = hashCode * 59 + this.ReleaseDate.GetHashCode();
                if (this.TrackCount != null)
                    hashCode = hashCode * 59 + this.TrackCount.GetHashCode();
                if (this.UpdatedAt != null)
                    hashCode = hashCode * 59 + this.UpdatedAt.GetHashCode();
                return hashCode;
            }
        }

        /// <summary>
        /// To validate all properties of the instance
        /// </summary>
        /// <param name="validationContext">Validation context</param>
        /// <returns>Validation Result</returns>
        IEnumerable<System.ComponentModel.DataAnnotations.ValidationResult> IValidatableObject.Validate(ValidationContext validationContext)
        {
            yield break;
        }
    }

}
```